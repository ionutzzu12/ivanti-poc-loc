---
title: Windowsデバイスの導入
createdAt: Wed Feb 11 2026 17:32:25 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:25 GMT+0200 (Eastern European Standard Time)
---

このセクションは以下のトピックを含みます。

- [**概要**](./Windowsデバイスの導入.md)
- [**デバイス管理**](./Windowsデバイスの導入.md)
- [**Windows デバイス登録**](./Windowsデバイスの導入.md)
- [**Windows Update 管理**](./Windowsデバイスの導入.md)
- [**アプリの配布と管理**](./Windowsデバイスの導入.md)
- [**アプリ制御**](./Windowsデバイスの導入.md)
- [**Windows デバイス管理構成**](./Windowsデバイスの導入.md)
- [**Windows デバイス コンプライアンス**](./Windowsデバイスの導入.md)
- [**Windows アプリおよびハードウェア インベントリ**](./Windowsデバイスの導入.md)

## 概要

Ivanti Neurons for MDM では、構成、登録、プロビジョニング、保護、アプリケーション、管理、監視、ソフトウェア更新、OS 更新、除却までの HoloLens 2 エンドツーエンド デバイス ライフサイクル管理を含む、すべての Windows ノート PC およびデスクトップ PC を管理できます。

## デバイス管理

サポートされている Windows デバイス:

- Windows PC 10+
- Microsoft HoleLens 2

デバイス管理とレポート機能の詳細については、[**デバイス**](./デバイス.md)をご参照ください。

## Windows デバイス登録

Ivanti Neurons for MDM は、次のような、Windowsデバイス用の標準的なデバイス登録方法をすべてサポートしています。

- 手動登録
- バルク登録
- SCCM と Ivanti EPM の使用
- Windows Autopilot
- Entra ID登録

登録方法の詳細については、[**Microsoft Azureの使用**](./Microsoft_Azureの使用.md)を参照してください。

マルチユーザーサポートについては、[**Windowsデバイスにおけるマルチユーザーサポート**](./Microsoft_Azureの使用.md)を参照してください。

## Windows Update 管理

- Windows update の構成とスケジュール - Windows update を構成してスケジュール設定するには、構成 - [**ソフトウェア更新**](./ソフトウェア更新.md)を使用して構成を作成します。
- Windows Update管理 - Windows Update管理を使用して更新するWindowsデバイスによって報告された更新を、表示して承認できます。 この機能では、不要またはテスト済みでない更新がデバイスにインストールされるのを防止します。 詳細については、[**Windows Update 管理**](Windows_Update_Management.htm)を参照してください。

## アプリの配布と管理

ユーザは、Windows アプリケーションのアプリ ライフサイクル全体 (インポート、構成、スケジュール、配布、更新、削除) を管理できます。

サポートされているアプリタイプ: 

- 自社開発
- MSB
- 公開ストア

サポートされているアプリ拡張:

- MSI
- MSIX
- APPX
- APPX バンドル
- EXE (Bridge)

Windows アプリの管理の詳細については、[**アプリ構成**](./アプリ構成.md)をご参照ください。 アプリ更新を自動化するには、[**Windowsアプリスケジューリング**](./Windowsアプリスケジューリング.md)および[**構成の操作**](./構成の操作.md)をご参照ください。

## アプリ制御

アプリ制御構成により、アプリをデバイスレベルで許可リストまたはブロックリストに分類できます。 すでにインストールされているアプリは非表示になり、起動できなくなります。 App Storeには引き続きアプリが表示されますが、ダウンロードや起動はできません。 アプリ制御構成が配布されたデバイスはすべて、この構成を使用し、許可されたアプリポリシー設定を無視します。 アプリ制御構成は、対象デバイス上で同じアプリを参照するアプリ関連ポリシーすべてに優先します。

詳細については、[**アプリ制御構成：デバイスごとにインストールするアプリを制御**](./アプリ制御構成：デバイスごとにインストールするアプリを制御.md)をご参照ください。

## Windows デバイス管理構成

Windows 10+ PC および Microsoft HoloLens 2 のサポートには次の機能が含まれています。

- [**デバイスの登録（Windows 10+のPCおよびMicrosoft Hololens 2）**](./デバイスの登録（Windows_10_のPCおよびMicrosoft_Hololens_2）.md)
- [**パスコード構成**](./パスコード構成.md)
- [**Exchange構成**](./Exchange構成.md)
- [**設定**](./設定.md)
- [**デバイス**](./デバイス.md)
- [**アプリ**](./アプリ.md)
- [**Windowsアプリスケジューリング**](./Windowsアプリスケジューリング.md)
- [**アプリ制御構成：デバイスごとにインストールするアプリを制御**](./アプリ制御構成：デバイスごとにインストールするアプリを制御.md)
- [**Windows Update 管理**](Windows_Update_Management.htm)
- [**Ivanti Neurons for MDM から Azure へのデバイス ステータスの報告**](./Ivanti_Neurons_for_MDM_から_Azure_へのデバイス_ステータスの報告.md)
- [**Windows Autopilotプロファイルの構成**](./Windows_Autopilotプロファイルの構成.md)
- [**カスタム構成を使用したデバイスへのSyncMLプッシュ**](./カスタム構成を使用したデバイスへのSyncMLプッシュ.md)
- [**ポリシー**](./ポリシー.md)
- Windows の制約
- ID 証明書
- Windows Hello for Business
- Wi-Fi および VPN プロファイル

このデバイスタイプによってサポートされていないHoloLensデバイスに配布された構成は、\[デバイスの詳細] の \[構成] タブに、配布済みの構成として報告されません。

Windows 機能 (Windows PC でのみサポート):

- [**Ivanti Bridge**](./Ivanti_Bridge.md)
- [**Windows BIOS構成**](./Windows_BIOS構成.md)
- [**Windows BitLocker**](./Windows_BitLocker.md)
- [**Windowsキオスク構成**](./Windowsキオスク構成.md)
- [**Windowsライセンス構成**](./Windowsライセンス構成.md)
- [**EMAサーバー統合構成**](./EMAサーバー統合構成.md)
- [**プリンター設定**](./プリンター設定.md)
- [**ブロートウェア削除構成**](./ブロートウェア削除構成.md)
- [**ADMX（GPO）ブラウザ**](./ADMX（GPO）ブラウザ.md)

## Windows デバイス コンプライアンス

Microsoft Azureで Ivanti Neurons for MDM を設定すると、Windows 10を実行するWindowsデスクトップとタブレットを使用するユーザーがシームレスに登録できます。 Azure テナント統合を構成して、Windows デバイス コンプライアンスを有効にするには、[**Microsoft Azureの使用**](./Microsoft_Azureの使用.md)をご参照ください。

## Windows アプリおよびハードウェア インベントリ

**Windows アプリ インベントリ**

アプリインベントリとは、登録されたデバイス上で検出されるアプリのリストです。 このページを利用して、登録されたデバイスで使用されるアプリに関する情報を取得します。 詳細については、[**アプリのインベントリ**](./アプリのインベントリ.md)をご参照ください。

デバイスのプライバシー構成により、そのデバイス上のすべてのアプリに関する情報の収集が許可されている場合は、そのデバイス上のWin32アプリまたはWin32ストアアプリが、アプリインベントリに表示されます。

**アプリインベントリ間隔の構成**

複数のアプリソースタイプのインベントリには、Windows 10アプリインベントリコレクション間隔を設定できます。 間隔は、デバイスからすべてのアプリを収集するようプライバシー構成が設定されている場合に使用します。

詳細については、[**アプリインベントリ間隔の構成**](./アプリインベントリ間隔の構成.md)をご参照ください。

**Windows ハードウェア インベントリ**
