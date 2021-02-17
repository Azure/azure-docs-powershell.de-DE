---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 4f484f200f2807cb814badbf93401061e670e72b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171767"
---
# Set-AzApiManagementAuthorizationServer

## SYNOPSIS
Ändert einen Autorisierungsserver.

## SYNTAX

```
Set-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzApiManagementAuthorizationServer"** ändert Die Details des Azure API Management Authorization Servers.

## BEISPIELE

### Beispiel 1: Ändern eines Autorisierungsservers
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

Dieser Befehl ändert den angegebenen API-Verwaltungsautorisierungsserver.

### Beispiel 2

Ändert einen Autorisierungsserver. (automatisch generiert)

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementAuthorizationServer -AccessTokenSendingMethods AuthorizationHeader -AuthorizationEndpointUrl 'https://contoso/authv2' -AuthorizationRequestMethods Get -ClientAuthenticationMethods Basic -ClientId 'clientid' -ClientRegistrationPageUrl 'https://contoso/signupv2' -ClientSecret '0000000000000000000000000000000000000' -Context <PsApiManagementContext> -DefaultScope <String> -GrantTypes AuthorizationCode -Name 'Contoso OAuth2 server' -ServerId 0123456789 -TokenEndpointUrl 'https://contoso/tokenv2'
```

## PARAMETERS

### -AccessTokenSendingMethods
Gibt ein Array von Methoden zum Senden eines Zugriffstokens an.
psdx_paramvalues AuthorizationHeader und Query.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationHeader, Query

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AuthorizationEndpointUrl
Gibt den Autorisierungsendpunkt an, um Ressourcenbesitzer zu authentifizieren und Autorisierungsermächtigungen zu erhalten.

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

### -AuthorizationRequestMethods
Gibt ein Array von Autorisierungsanforderungsmethoden an.
psdx_paramvalues "GET" und "POST" aus.
Der Standardwert ist "GET".

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Get, Post, Head, Options, Trace, Put, Patch, Delete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ClientAuthenticationMethods
Gibt ein Array von Clientauthentifizierungsmethoden an.
psdx_paramvalues "Basic" und "Body".

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Body

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ClientId
Gibt die Client-ID der Entwicklerkonsole an, bei der es sich um die Clientanwendung handelt.

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

### -ClientRegistrationPageUrl
Gibt den Clientregistrierungsendpunkt an, um Clients beim Autorisierungsserver zu registrieren und Clientanmeldeinformationen zu erhalten.

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

### -ClientSecret
Gibt den geheimen Clientgeheimnis der Entwicklerkonsole an, bei dem es sich um die Clientanwendung handelt.

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

### -Context
Gibt ein **"PsApiManagementContext"-Objekt** an.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -DefaultScope
Gibt den Standardbereich für den Autorisierungsserver an.

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

### -Beschreibung
Gibt eine Beschreibung für einen Autorisierungsserver an.

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

### -GrantTypes
Gibt ein Array von Granttypen an.
psdx_paramvalues
- AuthorizationCode
- ClientCredentials 
- Implizit 
- ResourceOwnerPassword

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationCode, Implicit, ResourceOwnerPassword, ClientCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des zu ändernden Autorisierungsservers an.

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

### -PassThru
passthru

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

### -ResourceOwnerPassword
Gibt das Kennwort des Ressourcenbesitzers an.
Sie müssen diesen Parameter angeben, wenn "ResourceOwnerPassword" durch den Parameter *"GrantTypes" angegeben* wird.

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

### -ResourceOwnerUsername
Gibt den Benutzernamen des Ressourcenbesitzers an.
Sie müssen diesen Parameter angeben, wenn "ResourceOwnerPassword" durch den Parameter *"GrantTypes" angegeben* wird.

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

### -ServerId
Gibt die ID des zu ändernden Autorisierungsservers an.

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

### -SupportState
Gibt an, ob der Parameter *"State" unterstützt werden* soll.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TokenBodyParameters
Gibt zusätzliche Textkörperparameter mithilfe des Formats "application/x-www-form-urlencoded" an.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TokenEndpointUrl
Gibt den Tokenendpunkt für Clients an, um Zugriffstoken im Austausch für die Präsentation von Autorisierungsermächtigungen oder Aktualisierungstokens abzurufen.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext

### System.String

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementModeltType[]

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]

### System.Collections.Hashtable

### System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]

### System.Management.Automation.SwitchParameter

## AUSGABEN

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzApiManagementAuthorizationServer](./Get-AzApiManagementAuthorizationServer.md)

[New-AzApiManagementAuthorizationServer](./New-AzApiManagementAuthorizationServer.md)

[Remove-AzApiManagementAuthorizationServer](./Remove-AzApiManagementAuthorizationServer.md)


