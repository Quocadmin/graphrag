# GraphRAG

👉 [Microsoft Research Blog Post](https://www.microsoft.com/en-us/research/blog/graphrag-unlocking-llm-discovery-on-narrative-private-data/)<br/>
👉 [Read the docs](https://microsoft.github.io/graphrag)<br/>
👉 [GraphRAG Arxiv](https://arxiv.org/pdf/2404.16130)

<div align="left">
  <a href="https://pypi.org/project/graphrag/">
    <img alt="PyPI - Version" src="https://img.shields.io/pypi/v/graphrag">
  </a>
  <a href="https://pypi.org/project/graphrag/">
    <img alt="PyPI - Downloads" src="https://img.shields.io/pypi/dm/graphrag">
  </a>
  <a href="https://github.com/microsoft/graphrag/issues">
    <img alt="GitHub Issues" src="https://img.shields.io/github/issues/microsoft/graphrag">
  </a>
  <a href="https://github.com/microsoft/graphrag/discussions">
    <img alt="GitHub Discussions" src="https://img.shields.io/github/discussions/microsoft/graphrag">
  </a>
</div>

## Overview

The GraphRAG project is a data pipeline and transformation suite that is designed to extract meaningful, structured data from unstructured text using the power of LLMs.

To learn more about GraphRAG and how it can be used to enhance your LLM's ability to reason about your private data, please visit the <a href="https://www.microsoft.com/en-us/research/blog/graphrag-unlocking-llm-discovery-on-narrative-private-data/" target="_blank">Microsoft Research Blog Post.</a>

## Quickstart

To get started with the GraphRAG system we recommend trying the [command line quickstart](https://microsoft.github.io/graphrag/get_started/).

## Repository Guidance

This repository presents a methodology for using knowledge graph memory structures to enhance LLM outputs. Please note that the provided code serves as a demonstration and is not an officially supported Microsoft offering.

⚠️ *Warning: GraphRAG indexing can be an expensive operation, please read all of the documentation to understand the process and costs involved, and start small.*

## Diving Deeper

- To learn about our contribution guidelines, see [CONTRIBUTING.md](./CONTRIBUTING.md)
- To start developing _GraphRAG_, see [DEVELOPING.md](./DEVELOPING.md)
- Join the conversation and provide feedback in the [GitHub Discussions tab!](https://github.com/microsoft/graphrag/discussions)

## Prompt Tuning

Using _GraphRAG_ with your data out of the box may not yield the best possible results.
We strongly recommend to fine-tune your prompts following the [Prompt Tuning Guide](https://microsoft.github.io/graphrag/prompt_tuning/overview/) in our documentation.

## Versioning

Please see the [breaking changes](./breaking-changes.md) document for notes on our approach to versioning the project.

*Always run `graphrag init --root [path] --force` between minor version bumps to ensure you have the latest config format. Run the provided migration notebook between major version bumps if you want to avoid re-indexing prior datasets. Note that this will overwrite your configuration and prompts, so backup if necessary.*

## Responsible AI FAQ

See [RAI_TRANSPARENCY.md](./RAI_TRANSPARENCY.md)

- [What is GraphRAG?](./RAI_TRANSPARENCY.md#what-is-graphrag)
- [What can GraphRAG do?](./RAI_TRANSPARENCY.md#what-can-graphrag-do)
- [What are GraphRAG’s intended use(s)?](./RAI_TRANSPARENCY.md#what-are-graphrags-intended-uses)
- [How was GraphRAG evaluated? What metrics are used to measure performance?](./RAI_TRANSPARENCY.md#how-was-graphrag-evaluated-what-metrics-are-used-to-measure-performance)
- [What are the limitations of GraphRAG? How can users minimize the impact of GraphRAG’s limitations when using the system?](./RAI_TRANSPARENCY.md#what-are-the-limitations-of-graphrag-how-can-users-minimize-the-impact-of-graphrags-limitations-when-using-the-system)
- [What operational factors and settings allow for effective and responsible use of GraphRAG?](./RAI_TRANSPARENCY.md#what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-graphrag)

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft
trademarks or logos is subject to and must follow
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.

## Privacy

[Microsoft Privacy Statement](https://privacy.microsoft.com/en-us/privacystatement)


GraphRAG là gì?
GraphRAG là một dự án mã nguồn mở của Microsoft, nhằm giúp các mô hình ngôn ngữ lớn (LLM – như ChatGPT, GPT-4…) hiểu và làm việc tốt hơn với dữ liệu văn bản tự do (unstructured text), ví dụ: email, báo cáo, tài liệu Word, ghi chú, v.v.

Thay vì chỉ trả lời dựa trên nội dung "thô", GraphRAG chuyển đổi dữ liệu văn bản này thành các cấu trúc dữ liệu dạng đồ thị tri thức (knowledge graph). Nhờ vậy, LLM sẽ dễ dàng tra cứu, phân tích và suy luận logic trên dữ liệu riêng của bạn.

Ứng dụng thực tế
Nếu bạn có một đống tài liệu và muốn dùng AI để tìm hiểu thông tin, đặt câu hỏi phức tạp, hoặc kết nối các dữ kiện lại với nhau, GraphRAG sẽ giúp bạn biến dữ liệu rời rạc thành một mạng lưới tri thức có thể tra cứu.

Ví dụ: Tìm các mối liên hệ giữa người – sự kiện – công ty trong hàng trăm trang tài liệu.

Cách hoạt động cơ bản
Nhập dữ liệu: Bạn đưa tài liệu vào hệ thống (file, text, v.v).

Trích xuất thông tin: GraphRAG dùng AI để phân tích văn bản, xác định các thực thể (người, tổ chức, sự kiện...) và mối quan hệ giữa chúng.

Xây dựng đồ thị tri thức: Dữ liệu này được tổ chức thành dạng "đồ thị" (nodes và edges), dễ dàng truy vấn và phân tích.

Tích hợp với LLM: Khi bạn hỏi AI, nó sẽ tham chiếu lên đồ thị tri thức này, giúp trả lời chính xác, logic và có dẫn chứng rõ ràng hơn.

Những điều cần lưu ý khi mới bắt đầu
Cài đặt nhanh: Có hướng dẫn quickstart để cài đặt và chạy thử bằng dòng lệnh.

Tài liệu: Đọc thêm tại Read the docs.

Lưu ý về chi phí: Việc index (phân tích và chuyển đổi dữ liệu) có thể tốn nhiều tài nguyên máy tính và thời gian, nhất là với dữ liệu lớn.

Hiệu quả sử dụng: Nếu muốn AI trả lời tốt hơn, nên tùy chỉnh prompt (hướng dẫn AI), theo hướng dẫn prompt tuning.

Phiên bản: Khi cập nhật phiên bản mới, nên làm theo hướng dẫn để tránh lỗi về cấu hình.

Trách nhiệm AI: Có tài liệu về AI minh bạch và có trách nhiệm.

Tóm tắt ngắn gọn
GraphRAG = "Đồ thị hóa dữ liệu văn bản + AI trả lời thông minh".

Dễ dàng trích xuất kiến thức từ dữ liệu riêng tư, phức tạp.

Hữu ích cho ai muốn xây dựng hệ thống hỏi đáp thông minh trên dữ liệu của doanh nghiệp/cá nhân.

Nếu bạn là người mới, hãy thử chạy demo nhỏ trước, đọc tài liệu và trao đổi trong mục Discussion trên GitHub repo để học hỏi thêm!
