---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-AzCloudServicePublicIPAddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
ms.openlocfilehash: 2a3b643a9ad9d9c588589003e5edb24ceddc4ae1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149036"
---
# Get-AzCloudServicePublicIPAddress

## SYNOPSIS
Holen Sie sich die öffentliche IP-Adresse eines Clouddiensts.

## SYNTAX

### CloudServiceName (Standard)
```
Get-AzCloudServicePublicIPAddress -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [<CommonParameters>]
```

### CloudService
```
Get-AzCloudServicePublicIPAddress -CloudService <CloudService> [-SubscriptionId <String>] [<CommonParameters>]
```

## BESCHREIBUNG
Holen Sie sich die öffentliche IP-Adresse eines Clouddiensts.

## BEISPIELE

### Beispiel 1: Öffentliche IP-Adressen auf Instanzebene für einen bestimmten Clouddienstnamen erhalten.
```powershell
PS C:\> Get-AzCloudServicePublicIPAddress -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

Ruft die öffentlichen IP-Adressen auf Instanzebene für einen bestimmten Clouddienstnamen ab.

### Beispiel 2: Öffentliche IP-Adressen auf Instanzebene für ein bestimmtes Clouddienstobjekt erhalten.
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServicePublicIPAddress -CloudService $cs

```

Ruft die öffentlichen IP-Adressen auf Instanzebene für ein bestimmtes Clouddienstobjekt ab.

## PARAMETERS

### -CloudService
CloudService-Instanz.
Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu #A0 und zum Erstellen einer Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudServiceName
CloudServiceName.

```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
ResourceGroupName.

```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Abonnement.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

## AUSGABEN

## HINWEISE

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften. Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.


<CloudService>CLOUDSERVICE: CloudService-Instanz.
  - `Location <String>`: Ressourcenspeicherort.
  - `[Configuration <String>]`: Gibt die XML-Dienstkonfiguration (CSCFG) für den Clouddienst an.
  - `[ConfigurationUrl <String>]`: Gibt eine URL an, die sich auf den Speicherort der Dienstkonfiguration im Blob Service bezieht. Bei der Dienstpaket-URL kann es sich um einen SAS-URI (Shared Access Signature) eines beliebigen Speicherkontos sein.         Dies ist eine schreib ausschließliche Eigenschaft, die nicht in GET-Aufrufen zurückgegeben wird.
  - `[ExtensionProfile <ICloudServiceExtensionProfile>]`: Beschreibt ein Clouddiensterweiterungsprofil.
    - `[Extension <IExtension[]>]`: Liste der Erweiterungen für den Clouddienst.
      - `[AutoUpgradeMinorVersion <Boolean?>]`: Geben Sie explizit an, ob die Plattform automatisch ein Upgrade von "typeHandlerVersion" auf höhere Nebenversionen durchführen kann, sobald diese verfügbar sind.
      - `[ForceUpdateTag <String>]`: Tag, um die Anwendung der bereitgestellten öffentlichen und geschützten Einstellungen zu erzwingen.         Wenn Sie den Tagwert ändern, können Sie die Erweiterung erneut ausführen, ohne die öffentlichen oder geschützten Einstellungen zu ändern.         Wenn "forceUpdateTag" nicht geändert wird, werden Updates an öffentlichen oder geschützten Einstellungen weiterhin vom Handler angewendet.         Wenn weder forceUpdateTag noch irgendeine der öffentlichen oder geschützten Einstellungen geändert wird, würde die Erweiterung zu der Rolleninstanz mit derselben Sequenznummer fließen, und es ist aufgabe der Handlerimplementierung, ob sie erneut ausgeführt werden soll oder nicht.
      - `[Name <String>]`: Der Name der Erweiterung.
      - `[ProtectedSetting <String>]`: Geschützte Einstellungen für die Erweiterung, die verschlüsselt werden, bevor sie an die Rolleninstanz gesendet werden.
      - `[ProtectedSettingFromKeyVaultSecretUrl <String>]`: 
      - `[Publisher <String>]`: Der Name des Herausgebers des Erweiterungshandlers.
      - `[RolesAppliedTo <String[]>]`: Optionale Liste der Rollen zum Anwenden dieser Erweiterung. Wenn keine Eigenschaft angegeben oder "*" angegeben wird, wird die Erweiterung auf alle Rollen im Clouddienst angewendet.
      - `[Setting <String>]`: Öffentliche Einstellungen für die Erweiterung. Bei JSON-Erweiterungen sind dies die JSON-Einstellungen für die Erweiterung. Bei einer XML-Erweiterung (wie RDP) ist dies die XML-Einstellung für die Erweiterung.
      - `[SourceVaultId <String>]`: Ressourcen-ID
      - `[Type <String>]`: Gibt den Typ der Erweiterung an.
      - `[TypeHandlerVersion <String>]`: Gibt die Version der Erweiterung an. Gibt die Version der Erweiterung an. Wenn dieses Element nicht angegeben ist oder ein Sternchen (*) als Wert verwendet wird, wird die neueste Version der Erweiterung verwendet. Wenn der Wert mit einer Hauptversionsnummer und einem Sternchen als Nebenversionsnummer (X.) angegeben ist, wird die neueste Nebenversion der angegebenen Hauptversion ausgewählt. Wenn eine Hauptversionsnummer und eine Nebenversionsnummer (X.Y) angegeben sind, wird die spezifische Erweiterungsversion ausgewählt. Wenn eine Version angegeben wird, wird für die Rolleninstanz ein automatisches Upgrade ausgeführt.
  - `[NetworkProfile <ICloudServiceNetworkProfile>]`: Netzwerkprofil für den Clouddienst.
    - `[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: Die Liste der Lastenausgleichskonfigurationen für den Clouddienst.
      - `[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Liste der IP
        - `[Name <String>]`: 
        - `[PrivateIPAddress <String>]`: Die private IP-Adresse, auf die der Clouddienst verwiesen hat.
        - `[PublicIPAddressId <String>]`: Ressourcen-ID
        - `[SubnetId <String>]`: Ressourcen-ID
      - `[Name <String>]`: Ressourcenname
    - `[SwappableCloudService <ISubResource>]`: 
      - `[Id <String>]`: Ressourcen-ID
  - `[OSProfile <ICloudServiceOSProfile>]`: Beschreibt das Betriebssystemprofil für den Clouddienst.
    - `[Secret <ICloudServiceVaultSecretGroup[]>]`: Gibt den Satz von Zertifikaten an, die auf den Rolleninstanzen installiert werden sollen.
      - `[SourceVaultId <String>]`: Ressourcen-ID
      - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`: Die Liste der Schlüsseltresorverweise in SourceVault, die Zertifikate enthalten.
        - `[CertificateUrl <String>]`: Dies ist die URL eines Zertifikats, das als geheimer Schlüssel in den Schlüsseltresor hochgeladen wurde.
  - `[PackageUrl <String>]`: Gibt eine URL an, die sich auf den Speicherort des Dienstpakets im Blob Service bezieht. Bei der Dienstpaket-URL kann es sich um einen SAS-URI (Shared Access Signature) eines beliebigen Speicherkontos sein.         Dies ist eine schreib ausschließliche Eigenschaft, die nicht in GET-Aufrufen zurückgegeben wird.
  - `[RoleProfile <ICloudServiceRoleProfile>]`: Beschreibt das Rollenprofil für den Clouddienst.
    - `[Role <ICloudServiceRoleProfileProperties[]>]`: Liste der Rollen für den Clouddienst.
      - `[Name <String>]`: Ressourcenname.
      - `[SkuCapacity <Int64?>]`: Gibt die Anzahl der Rolleninstanzen im Clouddienst an.
      - `[SkuName <String>]`: Der Name der SKU. HINWEIS: Wenn die neue SKU auf der Derzeit im Clouddienst verwendeten Hardware nicht unterstützt wird, müssen Sie den Clouddienst löschen und neu erstellen oder zur alten SKU zurück wechseln.
      - `[SkuTier <String>]`: Gibt die Stufe des Clouddiensts an. Mögliche Werte sind <br /><br /> **Standard** <br /><br /> **Standard**
  - `[StartCloudService <Boolean?>]`: (Optional) Gibt an, ob der Clouddienst sofort nach seiner Erstellen gestartet werden soll. Der Standardwert ist `true` " .         Wenn "false", wird das Dienstmodell noch bereitgestellt, aber der Code wird nicht sofort ausgeführt. Stattdessen wird der Dienst bis zum Startaufruf "PoweredOff" verwendet, zu dem der Dienst gestartet wird. Bei einem bereitgestellten Dienst fallen weiterhin Kosten an, auch wenn er nicht unterstützt wird.
  - `[Tag <ICloudServiceTags>]`: Ressourcentags.
    - `[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.
  - `[UpgradeMode <CloudServiceUpgradeMode?>]`: Updatemodus für den Clouddienst. Rolleninstanzen werden Domänen zugeordnet, wenn der Dienst bereitgestellt wird. Updates können manuell in jeder Updatedomäne oder automatisch in allen Updatedomänen initiiert werden.         Mögliche Werte sind <br /><br />**Auto**<br /><br />**Manuell** <br /><br />**Gleichzeitig**<br /><br />         Wenn keine Angabe ausgeführt wird, ist der Standardwert "Auto". Wenn dies auf "Manuell" festgelegt ist, muss PUT UpdateDomain aufgerufen werden, um das Update anzuwenden. Wenn dies auf "Automatisch" festgelegt ist, wird das Update automatisch auf jede Updatedomäne der Reihe nach angewendet.

## LINKS ZU VERWANDTEN THEMEN

