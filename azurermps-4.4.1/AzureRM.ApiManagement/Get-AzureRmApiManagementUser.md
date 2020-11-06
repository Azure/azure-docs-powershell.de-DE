---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: be6c9ee6c0db12e324786052348209703b79601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477449"
---
# Get-AzureRmApiManagementUser

## Synopsis
Ruft einen Benutzer oder Benutzer ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Alle Benutzer abrufen (Standard)
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Benutzer nach ID abrufen
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Suchen von Benutzern
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmApiManagementUser** " Ruft einen angegebenen Benutzer oder alle Benutzer ab, wenn kein Benutzer angegeben ist.

## Beispiele

### Beispiel 1: Abrufen aller Benutzer
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

Dieser Befehl ruft alle Benutzer ab.

### Beispiel 2: Abrufen eines Benutzers nach ID
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

Dieser Befehl ruft einen Benutzer nach ID ab.

### Beispiel: Abrufen von Benutzern nach Nachname
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

Mit diesem Befehl werden Benutzer mit dem angegebenen Nachnamen Fuller abgerufen.

### Beispiel 4: Abrufen eines Benutzers per e-Mail-Adresse
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email 
"user@contoso.com"
```

Mit diesem Befehl wird der Benutzer mit der angegebenen e-Mail-Adresse abgerufen.

### Beispiel 5: Abrufen aller Benutzer in einer Gruppe
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

Dieser Befehl ruft alle Benutzer in der angegebenen Gruppe ab.

## Parameter

### -Context
Gibt eine Instanz von **PsApiManagementContext** an.

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

### – E-Mail
Gibt die e-Mail-Adresse des Benutzers an.
Wenn dieser Parameter angegeben wird, findet ein Benutzer durch dieses Cmdlet eine e-Mail.
Dieser Parameter ist optional.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FirstName
Gibt den Vornamen des Benutzers an.
Wenn dieser Parameter angegeben wird, findet dieses Cmdlet einen Benutzer mit dem Vornamen.
Dieser Parameter ist optional.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Gruppen-Nr
Gibt die Gruppen-ID an.
Falls angegeben, findet dieses Cmdlet alle Benutzer in der angegebenen Gruppe.
Dieser Parameter ist optional.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nachname
Gibt den letzten Namen eines Benutzers an.
Falls angegeben, findet dieses Cmdlet Benutzer nach Nachname.
Dieser Parameter ist optional.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bundesland
Gibt den Benutzerstatus an.
Falls angegeben, findet dieses Cmdlet Benutzer in diesem Zustand.
Dieser Parameter ist optional.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: Find users
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserID
Gibt eine Benutzer-ID an.
Bei Angabe dieses Cmdlets findet der Benutzer diesen Bezeichner.
Dieser Parameter ist optional.

```yaml
Type: System.String
Parameter Sets: Get user by ID
Aliases: 

Required: False
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

### IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUser>

## Notizen

## Verwandte Links

[Neu – AzureRmApiManagementUser](./New-AzureRmApiManagementUser.md)

[Remove-AzureRmApiManagementUser](./Remove-AzureRmApiManagementUser.md)

[Satz-AzureRmApiManagementUser](./Set-AzureRmApiManagementUser.md)


