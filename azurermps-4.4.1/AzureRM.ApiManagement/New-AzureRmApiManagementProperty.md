---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: cb50ea5735a9f63f5f35b8f1cb0648c566e6108d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664491"
---
# New-AzureRmApiManagementProperty

## Synopsis
Erstellt eine neue Eigenschaft.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tags <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmApiManagementProperty** erstellt eine Azure API-Verwaltungs **Eigenschaft**.

## Beispiele

### Beispiel 1: Erstellen einer Eigenschaft, die Tags enthält
```
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

Der erste Befehl weist der $Tags Variablen zwei Werte zu.

Der zweite Befehl erstellt eine Eigenschaft und weist die Zeichenfolgen in $Tags als Tags für die Eigenschaft zu.

### Beispiel 2: Erstellen einer Eigenschaft mit einem geheimen Wert
```
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

Mit diesem Befehl wird eine **Eigenschaft** erstellt, die über einen verschlüsselten Wert verfügt.

## Parameter

### -Context
Gibt ein **PsApiManagementContext** -Objekt an.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der vom Cmdlet erstellten Eigenschaft an.
Die maximale Länge beträgt 100 Zeichen.
Namen enthalten nur Buchstaben, Ziffern, Punkt Zeichen, Striche und Unterstriche.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Eigenschafts-Nr
Gibt eine ID für die Eigenschaft an.
Die maximale Länge beträgt 256 Zeichen.
Wenn Sie keine ID angeben, generiert dieses Cmdlet eine.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Secret
Gibt an, dass der Eigenschaftswert ein Schlüssel ist und verschlüsselt werden sollte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tags
Gibt ein Array von Tags an, die dieses Cmdlet der Eigenschaft zuordnet.
Sie können Kategorien verwenden, um die Eigenschaftenliste zu filtern.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Wert
Gibt einen Wert für die Eigenschaft an.
Dieser Wert kann Richtlinienausdrücke enthalten.
Die maximale Länge beträgt 1000 Zeichen.
Der Wert darf nicht leer sein oder nur aus Leerzeichen bestehen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProperty

## Notizen

## Verwandte Links

[Remove-AzureRmApiManagementProperty](./Remove-AzureRmApiManagementProperty.md)

[Satz-AzureRmApiManagementProperty](./Set-AzureRmApiManagementProperty.md)


