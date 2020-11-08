---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BDCD6FD8-F4D5-4897-BF91-C78773DD3546
online version: ''
schema: 2.0.0
ms.openlocfilehash: f414f480328d508f0178d2536d144dceda3baab6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005719"
---
# New-AzureStorSimpleStorageAccountCredential

## Synopsis
Fügt eine Azure Storage Access-Anmeldeinformationen hinzu.

## Syntax

```
New-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> -StorageAccountKey <String>
 -UseSSL <Boolean> [-Endpoint <String>] [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureStorSimpleStorageAccountCredential** fügt dem StorSimple-Manager eine Azure-Speicherzugriffs Berechtigung zur Verwendung durch StorSimple OneSDK-Cmdlets hinzu.
Die meisten StorSimple-OneSDK-Cmdlets befassen sich mit Entitäten, die schließlich an ein bestimmtes Speicherkonto gebunden sind, wie Volumes, Volumen Container, Backups und Sicherungsrichtlinien.
Bei einigen Cmdlets müssen Sie die Anmeldeinformationen des verwendeten speicherkontos angeben.
Eine Speicherkonto Anmeldeinformationen ist ein in OneSDK erstelltes Access-Objekt, das auf ein vorhandenes Azure Storage-Konto verweist.
Sie geben den Namen und den Zugriffsschlüssel eines vorhandenen speicherkontos an, um eine Speicherkonto Anmeldeinformationen zu erstellen.
Sie können dieses Anmeldeinformationsobjekt dann mit anderen Cmdlets verwenden.

Dieses Cmdlet verwendet den Registrierungsschlüssel, den Sie angeben, wenn Sie die Ressource mithilfe des Cmdlets **Select-AzureStorSimpleResource** auswählen.
Stellen Sie sicher, dass der Wert richtig ist, um einen Verschlüsselungsfehler zu vermeiden.
Wenn Sie den Registrierungsschlüssel auf einen korrekten Wert ändern möchten, verwenden **Sie SELECT-AzureStorSimpleResource**.

## Beispiele

### Beispiel 1: Erstellen von Anmeldeinformationen
```
PS C:\>New-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoAccount07" -StorageAccountKey "L/eVcHtvqKjPWm5SaAJXtDlc0d69yVs0ICoZ2XIV1x0r9TqUyQyLUNS8lHvTvRmzdvQhJelav3fYyX7wyAu/SA==" -UseSSL $False -WaitForComplete
VERBOSE: ClientRequestId: f363cda4-54aa-4ee8-a3fa-00651ac86ffb_PS
VERBOSE: Found storage account with name : ContosoAccount07
VERBOSE: Storage credential verification succeeded. 
VERBOSE: ClientRequestId: 716ce6df-62b3-4d48-8e0e-b0c94eec6934_PS
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: 19aa4ef7-2789-4817-980c-19e33d257650_PS

JobId        : 84f74c25-b742-452c-973c-43c7446e9f49
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 72bcdf37-bf06-4dac-adc9-31bb8d06475a_PS
CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : b9986714-cef4-4c3f-a719-7acfc9559320
IsDefault                        : False
Location                         : West Europe
Login                            : ContosoAccount07
Name                             : ContosoAccount07
OperationInProgress              : None

Password                         : G1sBQ6/qAN1gyRGRZVarpi7o6ToJl61sGugfeJ75yx7cwyaGLQHjrSEEwhxThbDJkxso2emAOarTe920Uufy
                                   0AmJ9NpBI5hNyIFfwS4Ff+z2WmfKOzApyeofW5Zy7GPufehe/2ondq0XG4pGt3qxHFXNVUuiaPSU6TVWEKSh
                                   hWDaksSXYMGij3DJdZDW1MA49e6Q7OY+rFujbYvi9P2OjVj8T+FbiMtMB5NnQEqE+t3k74RqPIDKU+d3h9x4
                                   rYbAksGPfMvSa0fUipwYJ+Y5/NABA6j/MfB2pNDJbvqDoa1JCX6SKiwL81wmTh78/KnDY5ST3Said5DzKEbR
                                   iYMQZg==
PasswordEncryptionCertThumbprint : 
UseSSL                           : False
VolumeCount                      : 0
```

Dieser Befehl erstellt eine Speicherzugriffs Berechtigung für das angegebene Speicherkonto.
Dieser Befehl gibt den *WaitForComplete* -Parameter an, und das Cmdlet wartet so lange, bis der Vorgang abgeschlossen ist, um die Steuerung an die Konsole zurückzugeben.

### Beispiel 2: Erstellen von Anmeldeinformationen und Abfragen des Status der Aufgabe
```
PS C:\>New-AzureStorSimpleStorageAccountCredential -Name "ContosoAccount08" -Key "6BlMpSVrCQVQy3iOpkxiyY8uk/e3PiHIhadxV4qpPlKInr/eRFrGcWKDrfNC1IHj6oh0If/h3rALdZ0zuaf9cQ==" -UseSSL $True
PS C:\> Get-AzureStorSimpleTask -InstanceId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: 6104a834-ea57-4687-8e0b-1d97dc1c038b_PS
VERBOSE: Found storage account with name : ContosoAccount08
VERBOSE: Storage credential verification succeeded. 
VERBOSE: ClientRequestId: 1f686fa4-5afc-43c3-87b6-f2da7bf9e65f_PS
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: 8acb3770-bd72-43e6-9622-481002ad40b0_PS
53816d8d-a8b5-4c1d-a177-e59007608d6d
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
53816d8d-a8b5-4c1d-a177-e59007608d6d for tracking the task's status
```

Der erste Befehl erstellt eine Speicherzugriffs Berechtigung für das angegebene Speicherkonto.
Der Befehl gibt eine Aufgaben-ID zurück.

Der zweite Befehl fragt den Status der Aufgabe mit dem Cmdlet **Get-AzureStorSimpleTask** ab.
Der Befehl gibt die Aufgaben-ID aus dem ersten Befehl an.

### Beispiel 3: Erstellen von Anmeldeinformationen für die Verwendung mit einem anderen Cmdlet
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -Name "ContosoAccount09" | New-AzureStorSimpleDeviceVolumeContainer -Name "VC03" -DeviceName "Contoso63-AppVm" -BandWidthRate 256 -EncryptionEnabled $True -EncryptionKey "<your encryption key>" -WaitForComplete
VERBOSE: ClientRequestId: b1d1e637-cd72-4a1e-95a8-4db1d0b921a7_PS
VERBOSE: ClientRequestId: 71f56ca0-1f0b-4655-9331-4849e096345a_PS
VERBOSE: ClientRequestId: fbdd5a96-c95f-4547-9bcd-376d05543348_PS
VERBOSE: Storage Access Credential with name ContosoAccount09 found! 
VERBOSE: ClientRequestId: b44e0363-9979-4e97-aeb1-d9eb4073a337_PS
VERBOSE: ClientRequestId: a6047943-b01e-44e4-a91d-5103aa80ce57_PS
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: ac2dfd8b-922f-4e4d-8c8d-df1e2f87806c_PS


JobId        : 1cf2db5d-624f-46c4-97b9-c36451ba144e
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 9558414b-0883-4cf6-8a02-40efc7edd80d_PS
BandwidthRate                   : 256
EncryptionKey                   : g53NTgCF3SBVZzzk+9yUz5nZopvZpNr3th92ol7WRO7ZUKhodPm7WNjjHEKB0/V+JY6P68tdaF4JxF5jH58e/
                                  mCtTvnPNpOxykYFdY9GKGd9gnf+36sUPqiLFP+ONO5nN/N/zFmOeyuySsaa3gJsZG8eIiFc821yfe9m5QPbF
                                  bx/Qyu8qLl1R1LrKU7k+46IXfwQYSyclztydyuzvFUUic9kaJuR3944VLvrjvxJIbnLrYy7hsn+Gfq7ds9NFq
                                  AUILBH0+bk2uWgUlofAcE8fJ/rzDAHr8nFGWxOTJSrqAo0J3st8BN39+BcrY+zOWsMc/vKfc+Ss5PsGVGDT1r
                                  eQ==
InstanceId                      : 60c34706-ef0c-4c6f-ad90-7249f42648f7
IsDefault                       : False
IsEncryptionEnabled             : True
Name                            : VC03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 0
```

Mit diesem Befehl werden die Anmeldeinformationen für das Speicherkonto erstellt.
Der Befehl übergibt diese Anmeldeinformationen dann mithilfe des Pipelineoperators an das Cmdlet **New-AzureStorSimpleDeviceVolumeContainer** .
Dieses Cmdlet erstellt mithilfe der Anmeldeinformationen einen neuen Volumen Container.

## Parameter

### -Endpunkt
Gibt den Azure-Speicher Endpunkt für das Speicherkonto an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt ein Azure-Profil an.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
Gibt die Zugriffstaste des speicherkontos als nur-Text an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Gibt den Namen eines vorhandenen speicherkontos an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseSSL
Gibt an, ob SSL für die Verbindung bei Verwendung der neuen Anmeldeinformationen für das Speicherkonto verwendet werden soll.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForComplete
Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### IEnumerable \<StorageAccountCredentialResponse\> , TaskResponse
Wenn Sie den *WaitForComplete* -Parameter angeben, gibt dieses Cmdlet eine Liste von **StorageAccountCredentialResponse** -Objekten zurück.
Wenn Sie diesen Parameter nicht angeben, gibt das Cmdlet ein **TaskResponse** -Objekt zurück.
Eine **StorageAccountCredentialResponse** enthält die folgenden Eigenschaften: 

- **Cloudtype** ( **cloudtype** )
- **Hostname** ( **Zeichenfolge** )
- **InstanceId** ( **Zeichenfolge** )
- **IsDefault** ( **boolescher** Wert)
- **Ort** ( **Zeichenfolge** )
- **Login** ( **Zeichenfolge** )
- **Name** ( **Zeichenfolge** )
- **OperationInProgress** ( **OperationInProgress** )
- **Kennwort** ( **Zeichenfolge** )
- **PasswordEncryptionCertThumbprint** ( **Zeichenfolge** )
- **UseSSL** ( **boolescher Wert** )
- **VolumeCount** ( **int** )

## Notizen

## Verwandte Links

[Get-AzureStorSimpleStorageAccountCredential](./Get-AzureStorSimpleStorageAccountCredential.md)

[Remove-AzureStorSimpleStorageAccountCredential](./Remove-AzureStorSimpleStorageAccountCredential.md)

[Satz-AzureStorSimpleStorageAccountCredential](./Set-AzureStorSimpleStorageAccountCredential.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)

[Neu – AzureStorSimpleDeviceVolumeContainer](./New-AzureStorSimpleDeviceVolumeContainer.md)


