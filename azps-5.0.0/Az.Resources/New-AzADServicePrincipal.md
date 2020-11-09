---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 6d268c2378c93bcfb98e64c654880e8055bcede8
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/05/2020
ms.locfileid: "94303969"
---
# New-AzADServicePrincipal

## Synopsis
Erstellt einen neuen Azure Active Directory-Dienstprinzipal.

## Syntax

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

## Beschreibung

Erstellt einen neuen Azure Active Directory-Dienstprinzipal. Der Standardparametersatz verwendet Standardwerte für Parameter, wenn diese nicht bereitgestellt werden. Weitere Informationen zu Standardwerten finden Sie in der Beschreibung für jeden Parameter. Dieses Cmdlet hat die Möglichkeit, dem Dienstprinzipal eine Rolle mit den **Rollen** -und **Bereichs** Parametern zuzuweisen. Wenn beides ausgelassen wird, wird die Rolle des Mitwirkenden dem Dienstprinzipal zugewiesen. Die Standardwerte für die **Rollen** -und **Bereichs** Parameter sind **Mitwirkender** für das aktuelle Abonnement. Das Cmdlet erstellt eine Anwendung und legt ihre Eigenschaften fest, wenn keine ApplicationId bereitgestellt wird. Verwenden Sie das Cmdlet [Update-AzADApplication](./update-azadapplication.md) , um die anwendungsspezifischen Parameter zu aktualisieren.

> [!WARNING]
> Wenn Sie einen Dienstprinzipal mithilfe des Befehls **New-AzADServicePrincipal** erstellen, enthält die Ausgabe Anmeldeinformationen, die Sie schützen müssen. Stellen Sie sicher, dass Sie diese Anmeldeinformationen nicht in Ihren Code einbeziehen, oder überprüfen Sie die Anmeldeinformationen in die Quellcodeverwaltung. Als Alternative empfiehlt es sich, [verwaltete Identitäten](/azure/active-directory/managed-identities-azure-resources/overview) zu verwenden, um die Verwendung von Anmeldeinformationen zu vermeiden.
>
> Standardmäßig weist **New-AzADServicePrincipal** dem Dienstprinzipal im Abonnement Bereich die Rolle [Contributor](/azure/role-based-access-control/built-in-roles#contributor) zu. Um das Risiko eines kompromittierten Dienst Prinzipals zu verringern, weisen Sie eine spezifischere Rolle zu, und schränken Sie den Bereich auf eine Ressource oder eine Ressourcengruppe ein. Weitere Informationen finden Sie unter [Schritte zum Hinzufügen einer Rollenzuweisung](/azure/role-based-access-control/role-assignments-steps) .

## Beispiele

### Beispiel 1: Erstellen von einfachen AD-Dienst Prinzipalen

Im folgenden Beispiel wird ein Anzeigendienst Prinzipal mit Standardwerten für nicht angegebene Parameter erstellt. Da keine Anwendungs-ID bereitgestellt wird, wird eine Anwendung für den Dienstprinzipal erstellt. Da für **Rolle** oder **Bereich** keine Werte bereitgestellt werden, wird dem erstellten Dienstprinzipal die Rolle des **mitwirk** Enden für das aktuelle Abonnement zugewiesen.

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

### Beispiel 2: Erstellen eines einfachen AD-Dienst Prinzipals mit einer angegebenen Rolle und einem Standardbereich

Im folgenden Beispiel wird ein Ad-Dienstprinzipal mit den Standardwerten für nicht angegebene Parameter erstellt. Da die Anwendungs-ID nicht bereitgestellt wird, wird eine Anwendung für den Dienstprinzipal erstellt. Der Dienstprinzipal wird mit **Leser** Berechtigungen für das aktuelle Abonnement erstellt, da für den **Scope** -Parameter kein Wert angegeben wird.

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

### Beispiel 3: Erstellen eines einfachen AD-Dienst Prinzipals mit einem angegebenen Bereich und einer Standardrolle

Im folgenden Beispiel wird ein Ad-Dienstprinzipal mit den Standardwerten für nicht angegebene Parameter erstellt. Da die Anwendungs-ID nicht bereitgestellt wird, wird eine Anwendung für den Dienstprinzipal erstellt. Der Dienstprinzipal wird mit **Contributor** -Berechtigungen für den bereitgestellten Ressourcengruppen Bereich erstellt, da für den **Role** -Parameter kein Wert angegeben wird.

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

### Beispiel 4: Erstellen eines einfachen AD-Dienst Prinzipals mit einem angegebenen Bereich und einer bestimmten Rolle

Im folgenden Beispiel wird ein Ad-Dienstprinzipal mit den Standardwerten für nicht angegebene Parameter erstellt. Da die Anwendungs-ID nicht bereitgestellt wird, wird eine Anwendung für den Dienstprinzipal erstellt. Der Dienstprinzipal wird mit **Leser** Berechtigungen für den bereitgestellten Ressourcengruppen Bereich erstellt.

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

### Beispiel 5: Erstellen eines neuen Anzeigendienst Prinzipals mithilfe der Anwendungs-ID mit Rollenzuweisung

Im folgenden Beispiel wird ein neuer AD-Dienstprinzipal für die Anwendung mit der Anwendungs-ID "00000000-0000-0000-0000-000000000000" erstellt. Da für **Rolle** oder **Bereich** keine Werte bereitgestellt werden, wird dem erstellten Dienstprinzipal die Rolle des **mitwirk** Enden für das aktuelle Abonnement zugewiesen.

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

### Beispiel 6: Erstellen eines neuen AD-Dienst Prinzipals mithilfe von Piping

Im folgenden Beispiel wird die Anwendung mit der Objekt-ID "3ede3c26-b443-4e0b-9efc-b05e68338dc3" mit dem Cmdlet [Get-AzADApplication](./get-azadapplication.md) abgerufen. Die Ergebnisse werden an das `New-AzADServicePrincipal` Cmdlet umgeleitet, um einen neuen Anzeigendienst Prinzipal für diese Anwendung zu erstellen.

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### Beispiel 7: Erstellen eines neuen Anzeigendienst Prinzipals mithilfe von DisplayName und Kennwortanmeldeinformationen

Im folgenden Beispiel wird eine neue Anwendung mit dem Namen **servicePrincipalName** und dem Kennwort **StrongPassworld! 23** erstellt. Sie erstellt den Dienstprinzipal basierend auf der erstellten Anwendung. Das Startdatum und das Enddatum werden den Anmeldeinformationen für das Kennwort hinzugefügt.

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

### Beispiel 8: Erstellen eines neuen Anzeigendienst Prinzipals mit "DisplayName" und "Plain Key"-Anmeldeinformationen

Im folgenden Beispiel wird eine neue Anwendung mit dem Namen **servicePrincipalName** und einem Zertifikat **$CERT** erstellt. Sie erstellt den Dienstprinzipal basierend auf der erstellten Anwendung. Das Enddatum wird den Schlüssel Anmeldeinformationen hinzugefügt.

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

## Parameter

### -ApplicationId

Die eindeutige Anwendungs-ID für einen Dienstprinzipal in einem Mandanten. Nach der Erstellung kann diese Eigenschaft nicht geändert werden. Wenn keine Anwendungs-ID für eine vorhandene Anwendung angegeben wird, wird eine Anwendung erstellt.

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

Das Objekt, das die Anwendung darstellt, für die der Dienstprinzipal erstellt wird.

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

### -Certvalue

Der Wert des asymmetrischen Anmeldeinformationstyps. Es stellt das Base64-codierte Zertifikat dar.

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

### -DisplayName

Der Anzeigename des Dienst Prinzipals. Wenn kein Anzeigename angegeben wird, wird dieser Wert standardmäßig auf **Azure-PowerShell-mm-tt-yyyy-hh-mm-SS** gesetzt, wobei das Suffix der Zeitpunkt der Anwendungserstellung ist.

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

### -Enddate

Das effektive Enddatum der Anmelde Informationsverwendung. Der Standardwert für Enddatum beträgt ein Jahr ab heute.
Bei einer asymmetrischen typanmeldung muss dies auf ein oder vor dem Datum festgesetzt werden, an dem das X509-Zertifikat gültig ist.

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

### -Keycredential

Die Sammlung der wichtigen Anmeldeinformationen, die der Anwendung zugeordnet sind.

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

### -Role

Die Rolle, die der Dienstprinzipal über den Bereich hat. Wenn kein Wert angegeben wird, wird für **Role** standardmäßig die Rolle des **mitwirk** enden verwendet.

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

Der Bereich, für den der Dienstprinzipal über Berechtigungen verfügt. Wenn kein Wert angegeben wird, ist der **Bereich** standardmäßig auf das aktuelle Abonnement eingestellt.

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

Wenn diese Einstellung aktiviert ist, überspringen Sie das Erstellen der Standardrollenzuweisung für den Dienstprinzipal.

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

Der effektive Anfangstermin der Anmelde Informationsverwendung. Der Standardwert für das Anfangsdatum ist heute. Bei einer asymmetrischen typanmeldung muss dies auf ein oder nach dem Datum festgesetzt werden, ab dem das X509-Zertifikat gültig ist.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).
## Eingaben

### System. GUID

### System. String

### Microsoft. Azure. Commands. ActiveDirectory. PSADApplication

### Microsoft. Azure. Commands. ActiveDirectory. PSADPasswordCredential []

### Microsoft. Azure. Commands. ActiveDirectory. PSADKeyCredential []

### System. DateTime

## Ausgaben

### Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal

### Microsoft. Azure. Commands. resources. Models. Authorization. PSADServicePrincipalWrapper

## Notizen

Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung

## Verwandte Links

[Remove-AzADServicePrincipal](./Remove-AzADServicePrincipal.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

[Neu – AzADApplication](./New-AzADApplication.md)

[Remove-AzADApplication](./Remove-AzADApplication.md)

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

[Neu – AzADSpCredential](./New-AzADSpCredential.md)

[Remove-AzADSpCredential](./Remove-AzADSpCredential.md)