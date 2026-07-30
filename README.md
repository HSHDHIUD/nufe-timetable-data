# NUFE Timetable Data

南京财经大学（NUFE）教务系统公开教室课表接口的历史数据归档、行政班课表还原、专业课程矩阵和教师授课历史。

## 在线网站

- 课表查询站：[nufe-timetable-data.vercel.app](https://nufe-timetable-data.vercel.app)
- 完整数据 Release：[v2026.07.29](https://github.com/HSHDHIUD/nufe-timetable-data/releases/tag/v2026.07.29)

## 数据范围

- 接口可见学期：57 个，`1998-1999-1` 至 `2026-2027-1`
- 有课表数据并完成还原：33 个学期
- 全编号扫描无课表数据：24 个早期学期
- 班级课程实例：97,314 条
- 专业：146 个
- 历史教师：2,372 位
- 教师授课历史：111,861 条

完整扫描额外发现：

- `2008-2009-1`：1 条残留课程活动
- `2010-2011-2`：45 个有课教室、78 条课程活动

## 完整归档

完整数据以 GitHub Release 附件发布：

`nufe_timetable_authoritative_20260729.tar.gz`

归档包含：

- 所有有数据学期的原始教室 JSON
- 1998-2011 早期学期全编号扫描清单
- 各学期行政班/专业课表还原结果
- 最近两个完整学年及当前学期的班级周课表 HTML
- 全历史专业课程矩阵与最近两年课程矩阵
- 教师总表和教师授课历史
- 本项目使用的数据处理脚本

## 元数据

- `metadata/semester_coverage.csv`：57 个接口学期的扫描与还原状态
- `metadata/site_summary.json`：专业课程和班级课程统计
- `metadata/teacher_summary.json`：教师统计
- `metadata/unified_manifest.json`：统一目录清单

## 校验

下载 Release 附件后可用 `SHA256SUMS.txt` 校验完整性。

## 说明

数据来自无需登录即可访问的教务系统教室课表接口。专业课表由共享教室活动中的行政班信息还原；没有行政班关联的课程会保留在原始数据和教师历史中，但不会被强行归入某个专业。
