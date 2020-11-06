---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: 96b9b5a6bec10082d7b004dcede73b743a7e538b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502537"
---
# Get-AzureRmContext

## Synopsis
Ruft die Metadaten ab, mit denen Azure Resource Manager-Anforderungen authentifiziert werden.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Getsinglecontext (Standard)
```
Get-AzureRmContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### ListAllContexts
```
Get-AzureRmContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Get-AzureRmContext-Cmdlet ruft die aktuellen Metadaten ab, mit denen Azure-Ressourcen-Manager-Anforderungen authentifiziert werden.

Dieses Cmdlet ruft das Active Directory-Konto, den Active Directory-Mandanten, das Azure-Abonnement und die Ziel Azure-Umgebung ab.
Azure Resource Manager-Cmdlets verwenden diese Einstellungen standardmäßig beim Erstellen von Azure-Ressourcen-Manager-Anforderungen.

## Beispiele

### Beispiel 1: Abrufen des aktuellen Kontexts
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

In diesem Beispiel melden wir uns mit einem Azure-Abonnement mit Connect-AzureRmAccount bei unserem Konto an, und dann erhalten wir den Kontext der aktuellen Sitzung durch Aufrufen von Get-AzureRmContext.

### Beispiel 2: Auflisten aller verfügbaren Kontexte
```
PS C:\> Get-AzureRmContext -ListAvailable

Name                  : Test
Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :

Name                  : Production
Environment           : AzureCloud
Account               : prod@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Production Subscription
CurrentStorageAccount :
```

In diesem Beispiel werden alle derzeit verfügbaren Kontexte angezeigt.  Der Benutzer kann einen dieser Kontexte mithilfe von SELECT-AzureRmContext auswählen.

## Parameter

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

### -ListAvailable
Auflisten aller verfügbaren Kontexte in der aktuellen Sitzung.

```yaml
Type: SwitchParameter
Parameter Sets: ListAllContexts
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name des Kontexts

```yaml
Type: String
Parameter Sets: GetSingleContext
Aliases: 
Accepted values: Default

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### PSAzureContext
Dieses Cmdlet gibt das Konto, den Mandanten und das Abonnement zurück, das von Azure Resource Manager-Cmdlets verwendet wird.

## Notizen

## Verwandte Links

[Satz-AzureRMContext](./Set-AzureRMContext.md)

