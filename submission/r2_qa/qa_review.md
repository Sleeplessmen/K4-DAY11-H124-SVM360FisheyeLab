# QA review · B2-dense

Mã khóa: 8755-E75E

| frame | object_ref | rule_id | nhận xét |
|---|---|---|---|
| adasind_069450.jpg | L1 | R01 | Box xe Car ở xa có chiều cao H=22.4px < 40px, dưới ngưỡng kích thước bắt buộc của R01 |
| adasind_069450.jpg | L7 | R01 | Box Pedestrian có chiều cao H=22.1px < 40px, nằm ngoài phạm vi gán nhãn |
| adasind_117120.jpg | L9 | R01 | Box Car ở hậu cảnh có chiều cao H=21.9px < 40px, không đạt ngưỡng H=40 |
| adasind_062370.jpg | L7 | R05 | ThreeWheeler kích thước lớn ở mép khung hình cần rà soát lại attribute truncated |

# QA review · B2-mid

Mã khóa: 841F-339E

| frame | object_ref | rule_id | nhận xét |
|---|---|---|---|
| adasind_060000.jpg | L3 | R04 | Box L3 xe ThreeWheeler có class sai so với reference R4 |
| adasind_060000.jpg | R5 | R01 | Thiếu box L so với reference R5 (MISSING) |
| adasind_060000.jpg | R7 | R01 | Thiếu box L so với reference R7 (MISSING) |
| adasind_060000.jpg | R9 | R01 | Thiếu box L so với reference R9 (MISSING) |
| adasind_086220.jpg | L1 | R05 | Box L1 xe ThreeWheeler có thuộc tính cần rà soát so với reference R1 (ATTRIBUTE) |
| adasind_086220.jpg | R4 | R01 | Thiếu box L so với reference R4 (MISSING) |
| adasind_102750.jpg | L2 | R01 | Box L2 ThreeWheeler là spurious, dưới ngưỡng H=40 |
| adasind_102750.jpg | R2 | R01 | Thiếu box L so với reference R2 (MISSING) |
| adasind_102750.jpg | R4 | R01 | Thiếu box L so với reference R4 (MISSING) |
| adasind_102750.jpg | R5 | R01 | Thiếu box L so với reference R5 (MISSING) |

Ghi finding r2_qa: cell=L_only, rule_id có giá trị, why để trống.
