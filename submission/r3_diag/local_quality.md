# Đối chiếu chất lượng cục bộ — rectangle

Teaching reference, không phải gold set đã phê duyệt; không có điểm đạt tự động.
Nguồn: export r1_craft đã khóa SHA256 `9f19a663f5c5eb25448d97be3651f8dc22ef945d4cdd714886084ab7ed0b4724`; slice `B4-mid`.
Ghép hình học greedy một-một theo IoU ≥ 0.50, rồi so class; H ≥ 40 px.
Box trái nằm chủ yếu trong ignore_region reference không tính. Polygon, polyline, track không được chấm.
Đây là phép tính offline của lab, không phải báo cáo hay kết quả tương đương CVAT Premium.

Frame được tính: adasind_249480.jpg, adasind_261480.jpg, adasind_265065.jpg. Frame thiếu trong export: không.
TP=9; FP=0; FN=8; số lần đối chiếu=17; mean IoU của TP=0.895.

| Chỉ số | Micro | Macro | Nhãn thấp nhất |
|---|---:|---:|---:|
| accuracy | 0.529 | 0.906 | 0.765 |
| precision | 1.000 | 1.000 | 1.000 |
| recall | 0.529 | 0.627 | 0.200 |
| jaccard | 0.529 | 0.627 | 0.200 |
| dice | 0.692 | 0.717 | 0.333 |

| Nhãn | TP | FP | FN | Accuracy | Precision | Recall | Jaccard | Dice |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Bike | 3 | 0 | 2 | 0.882 | 1.000 | 0.600 | 0.600 | 0.750 |
| Car | 2 | 0 | 0 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 |
| Pedestrian | 1 | 0 | 4 | 0.765 | 1.000 | 0.200 | 0.200 | 0.333 |
| ThreeWheeler | 1 | 0 | 2 | 0.882 | 1.000 | 0.333 | 0.333 | 0.500 |
| Truck | 2 | 0 | 0 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 |

| Frame | TP | FP | FN | Accuracy | Precision | Recall |
|---|---:|---:|---:|---:|---:|---:|
| adasind_249480.jpg | 2 | 0 | 0 | 1.000 | 1.000 | 1.000 |
| adasind_261480.jpg | 5 | 0 | 2 | 0.714 | 1.000 | 0.714 |
| adasind_265065.jpg | 2 | 0 | 6 | 0.250 | 1.000 | 0.250 |

Confusion matrix: hàng = teaching reference; cột = export đã khóa.
`<missing>` là thiếu box; `<extra>` là box thừa. Xem `local_quality_confusion.csv`.

| Reference \ Export | Bike | Car | Pedestrian | ThreeWheeler | Truck | <missing> |
|---|---:|---:|---:|---:|---:|---:|
| Bike | 3 | 0 | 0 | 0 | 0 | 2 |
| Car | 0 | 2 | 0 | 0 | 0 | 0 |
| Pedestrian | 0 | 0 | 1 | 0 | 0 | 4 |
| ThreeWheeler | 0 | 0 | 0 | 1 | 0 | 2 |
| Truck | 0 | 0 | 0 | 0 | 2 | 0 |
| <extra> | 0 | 0 | 0 | 0 | 0 | 0 |

Chi tiết xung đột trong `local_quality_conflicts.csv`; dữ liệu máy đọc trong `local_quality.json`.
Mismatching label đóng góp một FP cho class vẽ và một FN cho class reference; attribute khác được báo riêng.
Micro accuracy đếm mỗi cặp ghép sai class là một lần đối chiếu; Jaccard đếm cả FP và FN.
Macro/worst bỏ nhãn không xuất hiện ở cả hai phía; chỉ số không có mẫu là N/A.
