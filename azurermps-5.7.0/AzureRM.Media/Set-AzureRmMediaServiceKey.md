---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/set-azurermmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
ms.openlocfilehash: 2b0e8564f2a536c7b7eda5b9ae8ae3cc58bf41cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662843"
---
# Set-AzureRmMediaServiceKey

## Synopsis
Regeneriert einen Schlüssel, der für den Zugriff auf den dem Mediendienst zugeordneten Ruhe Endpunkt verwendet wird.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmMediaServiceKey** " generiert einen Schlüssel, der für den Zugriff auf den mit dem Mediendienst verknüpften Repräsentations Status Transfer (Ruhe)-Endpunkt verwendet wird.

## Beispiele

### Beispiel 1: Erneutes Generieren des Primärschlüssels für den Zugriff auf den Mediendienst
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

Mit diesem Befehl wird der Primärschlüssel für den Mediendienst mit dem Namen MediaService001, der zur Ressourcengruppe mit dem Namen ResourceGroup004 gehört, erneut generiert.

### Beispiel 2: Erneutes Generieren des sekundären Schlüssels, der für den Zugriff auf den Mediendienst verwendet wird
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

Mit diesem Befehl wird der sekundäre Schlüssel für den Mediendienst mit dem Namen MediaService002, der zur Ressourcengruppe mit dem Namen Resourcegroup123 gehört, erneut generiert.

## Parameter

### -Kontoname
Gibt den Namen des Medien Diensts an, der vom Cmdlet erneut generiert wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -KeyType
Gibt den Schlüsseltyp des Medien Diensts an.
Die zulässigen Werte für diesen Parameter sind: primär oder sekundär.

```yaml
Type: KeyType
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. Media. Models. PSServiceKey

## Notizen

## Verwandte Links

[Get-AzureRmMediaServiceKeys](./Get-AzureRmMediaServiceKeys.md)


