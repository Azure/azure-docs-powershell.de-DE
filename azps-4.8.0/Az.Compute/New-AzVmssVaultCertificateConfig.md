---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 23b2b3acd5bb15771d3383cc39c6e0a69073a750
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173314"
---
# New-AzVmssVaultCertificateConfig

## Synopsis
Erstellt eine schlüsseltresor-Zertifikatkonfiguration.

## Syntax

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzVmssVaultCertificateConfig** gibt den geheimen Schlüssel an, der auf den virtuellen Computern des virtuellen Computers (Scale-Sets) gespeichert werden muss.
Die Ausgabe dieses Cmdlets ist für die Verwendung mit dem Add-AzVmssSecret-Cmdlet vorgesehen.

## Beispiele

### Beispiel 1: Erstellen einer schlüsseltresor-Zertifikatkonfiguration
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

Mit diesem Befehl wird eine Key Vault-Zertifikatkonfiguration erstellt, die den Zertifikatspeicher mit dem Namen mycerts verwendet, der sich unter der angegebenen Zertifikat-URL befindet.

## Parameter

### -CertificateStore
Gibt den Zertifikatspeicher auf den virtuellen Computern im Skalierungs Satz an, in dem das Zertifikat hinzugefügt wird.
Dies gilt nur für Skalierungs Sätze von Windows-virtuellen Computern.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl
Gibt den URI eines im schlüsseltresor gespeicherten Zertifikats an.
Es handelt sich um die Base64-Codierung des folgenden JSON-Objekts, das in UTF-8 codiert ist: {"Daten": " \<Base64-encoded-certificate\> ", "Datentyp": "PFX", "Kennwort": " \<pfx-file-password\> "}

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Management. Compute. Models. VaultCertificate

## Notizen

## Verwandte Links

[Add-AzVmssSecret](./Add-AzVmssSecret.md)
