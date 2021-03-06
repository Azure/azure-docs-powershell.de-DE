---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: f826ecbde81bc301cc51e031b2047bc7a9f284e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937403"
---
# New-AzADServicePrincipal

## SYNOPSIS
Erstellt einen neuen Azure Active Directory-Dienstprinzipal.

## SYNTAX

### SimpleParameterSet (Standard)

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithoutCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ApplicationWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyPlainParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithoutCredentialParameterSet

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DisplayNameWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyPlainParameterSet

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyCredentialParameterSet

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyPlainParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG

Erstellt einen neuen Azure Active Directory-Dienstprinzipal. Der Standardparametersatz verwendet Standardwerte für Parameter, wenn diese nicht bereitgestellt werden. Weitere Informationen zu Standardwerten finden Sie in der Beschreibung für jeden Parameter. Dieses Cmdlet kann dem Dienstprinzipal mit den  Parametern Rolle und Bereich eine **Rolle** zuweisen. Fehlt beides, wird dem Dienstprinzipal die Mitwirkenderolle zugewiesen. Die Standardwerte für die **Parameter Rolle** und **Bereich** sind **Mitwirkender** für das aktuelle Abonnement. Das Cmdlet erstellt eine Anwendung und legt deren Eigenschaften fest, wenn keine ApplicationId bereitgestellt wird. Verwenden Sie zum Aktualisieren der anwendungsspezifischen Parameter das [Cmdlet Update-AzADApplication.](./update-azadapplication.md)

> [!WARNING]
> Wenn Sie einen Dienstprinzipal mit dem **Befehl New-AzADServicePrincipal erstellen,** enthält die Ausgabe Anmeldeinformationen, die Sie schützen müssen. Als Alternative sollten Sie die Verwendung [verwalteter Identitäten in](/azure/active-directory/managed-identities-azure-resources/overview) Betracht ziehen, um die Verwendung von Anmeldeinformationen zu vermeiden.
>
> Standardmäßig weist **New-AzADServicePrincipal** dem [](/azure/role-based-access-control/built-in-roles#contributor) Dienstprinzipal im Abonnementbereich die Rolle "Mitwirkender" zu. Um das Risiko eines gefährdeten Dienstprinzipals zu verringern, weisen Sie einer Ressource oder Ressourcengruppe eine spezifischere Rolle zu, und verringern Sie den Bereich. Weitere [Informationen finden Sie unter Schritte zum Hinzufügen einer](/azure/role-based-access-control/role-assignments-steps) Rollenzuweisung.

## BEISPIELE

### Beispiel 1: Einfache Erstellung eines AD-Dienstprinzipals

Im folgenden Beispiel wird ein AD-Dienstprinzipal mit Standardwerten für Parameter erstellt, die nicht angegeben sind. Da keine Anwendungs-ID bereitgestellt wird, wird eine Anwendung für den Dienstprinzipal erstellt. Da für Rolle  oder Umfang keine Werte bereitgestellt **werden,** wird dem erstellten Dienstprinzipal die Mitwirkenderolle  für das aktuelle Abonnement zugewiesen.

```powershell
New-AzADServicePrincipal
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### Beispiel 2: Einfache Erstellung eines AD-Dienstprinzipals mit einer angegebenen Rolle und einem Standardbereich

Im folgenden Beispiel wird ein AD-Dienstprinzipal mit den Standardwerten für nicht angegebene Parameter erstellt. Da die Anwendungs-ID nicht bereitgestellt wird, wird eine Anwendung für den Dienstprinzipal erstellt. Der Dienstprinzipal wird mit **Leseberechtigungen** für das aktuelle Abonnement erstellt, da kein Wert für den Parameter **Scope bereitgestellt** wird.

```powershell
New-AzADServicePrincipal -Role Reader
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000' to the new service principal.
```

### Beispiel 3: Einfache Erstellung eines AD-Dienstprinzipals mit einem angegebenen Bereich und einer Standardrolle

Im folgenden Beispiel wird ein AD-Dienstprinzipal mit den Standardwerten für nicht angegebene Parameter erstellt. Da die Anwendungs-ID nicht bereitgestellt wird, wird eine Anwendung für den Dienstprinzipal erstellt. Der Dienstprinzipal wird mit **Mitwirkendenberechtigungen für** den bereitgestellten Ressourcengruppenbereich erstellt, da kein Wert für den Parameter **Rolle bereitgestellt** wird.

```powershell
New-AzADServicePrincipal -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### Beispiel 4: Einfache Erstellung eines AD-Dienstprinzipals mit einem angegebenen Bereich und einer bestimmten Rolle

Im folgenden Beispiel wird ein AD-Dienstprinzipal mit den Standardwerten für nicht angegebene Parameter erstellt. Da die Anwendungs-ID nicht bereitgestellt wird, wird eine Anwendung für den Dienstprinzipal erstellt. Der Dienstprinzipal wird mit **Leseberechtigungen für** den bereitgestellten Ressourcengruppenbereich erstellt.

```powershell
New-AzADServicePrincipal -Role Reader -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### Beispiel 5: Erstellen eines neuen AD-Dienstprinzipals mithilfe der Anwendungs-ID mit Rollenzuweisung

Im folgenden Beispiel wird ein neuer AD-Dienstprinzipal für die Anwendung mit der Anwendungs-ID '000000000-0000-0000-0000-0000000000000' erstellt. Da für Rolle  oder Umfang keine Werte bereitgestellt **werden,** wird dem erstellten Dienstprinzipal die Mitwirkenderolle  für das aktuelle Abonnement zugewiesen.

```powershell
New-AzADServicePrincipal -ApplicationId 00000000-0000-0000-0000-000000000000
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://my-temp-app}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : my-temp-app
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### Beispiel 6: Erstellen eines neuen AD-Dienstprinzipals mithilfe von Piping

Im folgenden Beispiel wird die Anwendung mit der Objekt-ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' mithilfe des [Get-AzADApplication-Cmdlets](./get-azadapplication.md) abgerufen. Die Ergebnisse werden an das `New-AzADServicePrincipal` Cmdlet gepipent, um einen neuen AD-Dienstprinzipal für diese Anwendung zu erstellen.

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### Beispiel 7: Erstellen eines neuen AD-Dienstprinzipals mit Anzeigename und Kennwortanmeldeinformationen

Im folgenden Beispiel wird eine neue Anwendung mit dem Namen **ServicePrincipalName** und einem Kennwort von **StrongPassworld!23 erstellt.** Er erstellt den Dienstprinzipal basierend auf der erstellten Anwendung. Das Startdatum und das Enddatum werden den Kennwortanmeldeinformationen hinzugefügt.

```powershell
$credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{
  StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password='StrongPassworld!23'}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000c
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

### Beispiel 8: Erstellen eines neuen AD-Dienstprinzipals mit DisplayName und Einfachschlüsselanmeldeinformationen

Im folgenden Beispiel wird eine neue Anwendung mit dem Namen **ServicePrincipalName** und einem Zertifikat **$cert.** Er erstellt den Dienstprinzipal basierend auf der erstellten Anwendung. Das Enddatum wird den Schlüsselanmeldeinformationen hinzugefügt.

```powershell
$cert = 'public certificate as Base64 encoded string'
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate '2021-01-01'
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

## PARAMETER

### -ApplicationId

Die eindeutige Anwendungs-ID für einen Dienstprinzipal in einem Mandanten. Nach dem Erstellen kann diese Eigenschaft nicht mehr geändert werden. Wenn keine Anwendungs-ID für eine vorhandene Anwendung angegeben wird, wird eine Anwendung erstellt.

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationObject

Das -Objekt, das die Anwendung darstellt, für die der Dienstprinzipal erstellt wird.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CertValue

Der Wert des asymmetrischen Anmeldeinformationstyps. Es stellt das base64-codierte Zertifikat dar.

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -DisplayName

Der Anzeigename des Dienstprinzipals. Wenn kein Anzeigename angegeben wird, wird dieser Wert standardmäßig **auf azure-powershell-MM-dd-yyyy-HH-mm-ss festgelegt,** wobei das Suffix der Zeitpunkt der Anwendungserstellung ist.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndDate

Das effektive Enddatum der Anmeldeinformationsverwendung. Der Standardwert für das Enddatum ist ein Jahr ab heute.
Bei asymmetrischen Typanmeldeinformationen muss dies auf am oder vor dem Datum festgelegt sein, an dem das X509-Zertifikat gültig ist.

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyCredential

Die Sammlung der Schlüsselanmeldeinformationen, die der Anwendung zugeordnet sind.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PasswordCredential

Die Sammlung der Kennwortanmeldeinformationen, die der Anwendung zugeordnet sind.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Rolle

Die Rolle, die der Dienstprinzipal über den Bereich hat. Wenn kein Wert angegeben wird, **wird "Rolle"** standardmäßig auf die Rolle **"Mitwirkender"** festgelegt.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope

Der Bereich, für den der Dienstprinzipal Berechtigungen besitzt. Wenn kein Wert angegeben wird, **wird der Bereich** standardmäßig auf das aktuelle Abonnement festgelegt.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipAssignment

Wenn festgelegt, überspringen Sie das Erstellen der Standardrollezuweisung für den Dienstprinzipal.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartDate

Das effektive Startdatum der Anmeldeinformationsverwendung. Der Standardwert für das Startdatum ist heute. Bei asymmetrischen Typanmeldeinformationen muss dies auf am oder nach dem Datum festgelegt sein, ab dem das X509-Zertifikat gültig ist.

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen

Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).
## EINGABEN

### System.Guid

### System.String

### Microsoft.Azure.Commands.ActiveDirectory.PSDApplication

### Microsoft.Azure.Commands.ActiveDirectory.PSDPasswordCredential[]

### Microsoft.Azure.Commands.ActiveDirectory.PSDKeyCredential[]

### System.DateTime

## AUSGABEN

### Microsoft.Azure.Commands.ActiveDirectory.PSDServicePrincipal

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSDServicePrincipalWrapper

## NOTIZEN

Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment

## VERWANDTE LINKS

[Remove-AzADServicePrincipal](./Remove-AzADServicePrincipal.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

[New-AzADApplication](./New-AzADApplication.md)

[Remove-AzADApplication](./Remove-AzADApplication.md)

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

[New-AzADSpCredential](./New-AzADSpCredential.md)

[Remove-AzADSpCredential](./Remove-AzADSpCredential.md)