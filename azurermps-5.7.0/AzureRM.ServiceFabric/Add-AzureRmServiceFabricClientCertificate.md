---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: c7b6e00ccbe368267fd6b110490df4f70b2229a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500394"
---
# Add-AzureRmServiceFabricClientCertificate

## Synopsis
Fügen Sie dem Cluster einen allgemeinen Namen oder Fingerabdruck hinzu, um Client Authentifizierungszwecke zu verwenden.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### SingleUpdateWithThumbprint
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SingleUpdateWithCommonName
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### MultipleUpdatesWithCommonName
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### MultipleUpdatesWithThumbprint
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Verwenden Sie **Add-AzureRmServiceFabricClientCertificate** , um dem Cluster einen allgemeinen Namen und einen ausstellenden Fingerabdruck oder Zertifikat Fingerabdruck hinzuzufügen, damit der Client ihn zur Authentifizierung verwenden kann.

## Beispiele

### Beispiel 1
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

Mit diesem Befehl wird dem Cluster das Zertifikat mit dem Fingerabdruck "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" hinzugefügt, sodass der Client das Zertifikat als Administrator für die Kommunikation mit dem Cluster verwenden kann.

### Beispiel 2
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

Mit diesem Befehl wird ein nur-Lese-Clientzertifikat hinzugefügt, dessen allgemeiner Name "contoso.com" und der Fingerabdruck des Ausstellers "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" ist.

## Parameter

### – Administrator
Client Authentifizierungs.

```yaml
Type: SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AdminClientThumbprint
Geben Sie den Fingerabdruck des Clientzertifikats an, der nur über Administratorberechtigungen verfügt.

```yaml
Type: String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ClientCertificateCommonName
Geben Sie den allgemeinen Clientnamen, den Aussteller Fingerabdruck und den Authentifizierungstyp an.

```yaml
Type: PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CommonName
Geben Sie den allgemeinen Namen des Clientzertifikats an.

```yaml
Type: String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IssuerThumbprint
Geben Sie den Fingerabdruck des Clientzertifikats heraus.

```yaml
Type: String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Geben Sie den Namen des Clusters an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReadonlyClientThumbprint
Geben Sie den Fingerabdruck des Clientzertifikats an, der nur die Berechtigung Lesen hat.

```yaml
Type: String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Fingerabdruck
Kunden Zertifikat-Fingerabdruck angeben.

```yaml
Type: String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. Collections. Hashtable
System. String

System. Boolean

## Ausgaben

### Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster

## Notizen

## Verwandte Links

[Remove-AzureRmServiceFabricClientCertificate](./Remove-AzureRmServiceFabricClientCertificate.md)
