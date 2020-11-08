---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7F51F534-6C64-4983-A08F-4732A39C2E7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c62f3d29b4cd2c87fd5606ca013eb03958fb62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006270"
---
# <span data-ttu-id="7382c-101">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="7382c-101">Set-AzureDeployment</span></span>

## <span data-ttu-id="7382c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7382c-102">SYNOPSIS</span></span>
<span data-ttu-id="7382c-103">Ändert den Status, die Konfigurationseinstellungen oder den Aktualisierungsmodus einer Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="7382c-103">Modifies the status, configuration settings, or upgrade mode of a deployment.</span></span>

## <span data-ttu-id="7382c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7382c-104">SYNTAX</span></span>

### <span data-ttu-id="7382c-105">Upgrade</span><span class="sxs-lookup"><span data-stu-id="7382c-105">Upgrade</span></span>
```
Set-AzureDeployment [-Upgrade] [-ServiceName] <String> [-Package] <String> [-Configuration] <String>
 [-Slot] <String> [[-Mode] <String>] [[-Label] <String>] [[-RoleName] <String>] [-Force]
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7382c-106">Config</span><span class="sxs-lookup"><span data-stu-id="7382c-106">Config</span></span>
```
Set-AzureDeployment [-Config] [-ServiceName] <String> [-Configuration] <String> [-Slot] <String>
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7382c-107">Status</span><span class="sxs-lookup"><span data-stu-id="7382c-107">Status</span></span>
```
Set-AzureDeployment [-Status] [-ServiceName] <String> [-Slot] <String> [-NewStatus] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="7382c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7382c-108">DESCRIPTION</span></span>
<span data-ttu-id="7382c-109">Mit dem Cmdlet " **festlegen-AzureDeployment** " werden der Status, die Konfigurationseinstellungen oder der Upgrademodus einer Azure-Bereitstellung geändert.</span><span class="sxs-lookup"><span data-stu-id="7382c-109">The **Set-AzureDeployment** cmdlet modifies the status, configuration settings, or upgrade mode of an Azure deployment.</span></span>
<span data-ttu-id="7382c-110">Sie können den Status der Bereitstellung entweder auf "ausgeführt" oder "angehalten" ändern.</span><span class="sxs-lookup"><span data-stu-id="7382c-110">You can change the status of the deployment to either Running or Suspended.</span></span>
<span data-ttu-id="7382c-111">Sie können die cscfg-Datei für die Bereitstellung ändern.</span><span class="sxs-lookup"><span data-stu-id="7382c-111">You can change the .cscfg file for the deployment.</span></span>
<span data-ttu-id="7382c-112">Sie können den Aktualisierungsmodus und Konfigurationsdateien aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7382c-112">You can set the upgrade mode and update configuration files.</span></span>
<span data-ttu-id="7382c-113">Verwenden Sie das Cmdlet " **Satz-AzureWalkUpgradeDomain** ", um ein Upgrade zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="7382c-113">Use the **Set-AzureWalkUpgradeDomain** cmdlet to initiate an upgrade.</span></span>

## <span data-ttu-id="7382c-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7382c-114">EXAMPLES</span></span>

### <span data-ttu-id="7382c-115">Beispiel 1: Ändern des Status einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="7382c-115">Example 1: Change the status of a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Status -ServiceName "ContosoService" -Slot "Production" -NewStatus "Running"
```

<span data-ttu-id="7382c-116">Dieser Befehl legt den Status der Bereitstellung für den Dienst mit dem Namen ContosoService in der Produktionsumgebung auf Running fest.</span><span class="sxs-lookup"><span data-stu-id="7382c-116">This command sets the status of the deployment for the service named ContosoService in the production environment to Running.</span></span>

### <span data-ttu-id="7382c-117">Beispiel 2: Zuweisen einer anderen Konfigurationsdatei zu einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="7382c-117">Example 2: Assign a different configuration file to a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Slot "Staging" -Configuration "C:\Temp\MyServiceConfig.Cloud.csfg"
```

<span data-ttu-id="7382c-118">Dieser Befehl weist in der Stagingumgebung eine andere Konfigurationsdatei für die Bereitstellung des Diensts mit dem Namen "ContosoService" zu.</span><span class="sxs-lookup"><span data-stu-id="7382c-118">This command assigns a different configuration file for the deployment for the service named ContosoService in the staging environment.</span></span>

### <span data-ttu-id="7382c-119">Beispiel 3: Einrichten des Upgrademodus auf "automatisch"</span><span class="sxs-lookup"><span data-stu-id="7382c-119">Example 3: Set the upgrade mode to Auto</span></span>
```
PS C:\> Set-AzureDeployment -Upgrade -ServiceName "ContosoService" -Mode Auto -Package "C:\packages\ContosoApp.cspkg" -Configuration "C:\Config\ContosoServiceConfig.Cloud.csfg"
```

<span data-ttu-id="7382c-120">Mit diesem Befehl wird der Aktualisierungsmodus auf Auto festgelegt, und es wird ein Upgrade-Paket und eine neue Konfigurationsdatei angegeben.</span><span class="sxs-lookup"><span data-stu-id="7382c-120">This command sets the upgrade mode to Auto, and specifies an upgrade package and a new configuration file.</span></span>

### <span data-ttu-id="7382c-121">Beispiel 4: Installieren der Erweiterungskonfiguration in einem Dienst</span><span class="sxs-lookup"><span data-stu-id="7382c-121">Example 4: Install extension configuration in a service</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Mode "Automatic" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Slot "Production" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="7382c-122">Mit diesem Befehl wird die Erweiterungskonfiguration im angegebenen cloudbasierten Dienst installiert und auf Rollen angewendet.</span><span class="sxs-lookup"><span data-stu-id="7382c-122">This command installs the extension configuration in the specified Cloud Service and applies them on roles.</span></span>

## <span data-ttu-id="7382c-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="7382c-123">PARAMETERS</span></span>

### <span data-ttu-id="7382c-124">-Config</span><span class="sxs-lookup"><span data-stu-id="7382c-124">-Config</span></span>
<span data-ttu-id="7382c-125">Gibt an, dass dieses Cmdlet die Konfiguration der Bereitstellung ändert.</span><span class="sxs-lookup"><span data-stu-id="7382c-125">Specifies that this cmdlet modifies the configuration of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Config
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7382c-126">-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="7382c-126">-Configuration</span></span>
<span data-ttu-id="7382c-127">Gibt den vollständigen Pfad einer cscfg-Konfigurationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="7382c-127">Specifies the full path of a .cscfg configuration file.</span></span>
<span data-ttu-id="7382c-128">Sie können eine Konfigurationsdatei für eine Upgrade-oder Konfigurationsänderung angeben.</span><span class="sxs-lookup"><span data-stu-id="7382c-128">You can specify a configuration file for an upgrade or configuration change.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade, Config
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7382c-129">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="7382c-129">-ExtensionConfiguration</span></span>
<span data-ttu-id="7382c-130">Gibt ein Array von Erweiterungs Konfigurationsobjekten an.</span><span class="sxs-lookup"><span data-stu-id="7382c-130">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: Upgrade, Config
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7382c-131">-Force</span><span class="sxs-lookup"><span data-stu-id="7382c-131">-Force</span></span>
<span data-ttu-id="7382c-132">Gibt an, dass das Cmdlet ein erzwungenes Upgrade ausführt.</span><span class="sxs-lookup"><span data-stu-id="7382c-132">Indicates that cmdlet performs a forced upgrade.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7382c-133">-Information</span><span class="sxs-lookup"><span data-stu-id="7382c-133">-InformationAction</span></span>
<span data-ttu-id="7382c-134">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="7382c-134">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7382c-135">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7382c-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7382c-136">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="7382c-136">Continue</span></span>
- <span data-ttu-id="7382c-137">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="7382c-137">Ignore</span></span>
- <span data-ttu-id="7382c-138">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="7382c-138">Inquire</span></span>
- <span data-ttu-id="7382c-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7382c-139">SilentlyContinue</span></span>
- <span data-ttu-id="7382c-140">Beenden</span><span class="sxs-lookup"><span data-stu-id="7382c-140">Stop</span></span>
- <span data-ttu-id="7382c-141">Anhalten</span><span class="sxs-lookup"><span data-stu-id="7382c-141">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7382c-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7382c-142">-InformationVariable</span></span>
<span data-ttu-id="7382c-143">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="7382c-143">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7382c-144">-Label</span><span class="sxs-lookup"><span data-stu-id="7382c-144">-Label</span></span>
<span data-ttu-id="7382c-145">Gibt eine Bezeichnung für die aktualisierte Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="7382c-145">Specifies a label for the upgraded deployment.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7382c-146">-Modus</span><span class="sxs-lookup"><span data-stu-id="7382c-146">-Mode</span></span>
<span data-ttu-id="7382c-147">Gibt den Aktualisierungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="7382c-147">Specifies the mode of upgrade.</span></span>
<span data-ttu-id="7382c-148">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7382c-148">Valid values are:</span></span> 

- <span data-ttu-id="7382c-149">Auto</span><span class="sxs-lookup"><span data-stu-id="7382c-149">Auto</span></span> 
- <span data-ttu-id="7382c-150">Manuell</span><span class="sxs-lookup"><span data-stu-id="7382c-150">Manual</span></span> 
- <span data-ttu-id="7382c-151">Gleichzeitiges</span><span class="sxs-lookup"><span data-stu-id="7382c-151">Simultaneous</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7382c-152">-Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="7382c-152">-NewStatus</span></span>
<span data-ttu-id="7382c-153">Gibt den Zielstatus für die Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="7382c-153">Specifies the target status for the deployment.</span></span>
<span data-ttu-id="7382c-154">Gültige Werte sind: wird ausgeführt und angehalten.</span><span class="sxs-lookup"><span data-stu-id="7382c-154">Valid values are: Running and Suspended.</span></span>

```yaml
Type: String
Parameter Sets: Status
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7382c-155">-Paket</span><span class="sxs-lookup"><span data-stu-id="7382c-155">-Package</span></span>
<span data-ttu-id="7382c-156">Gibt den vollständigen Pfad einer Upgrade-Paketdatei an.</span><span class="sxs-lookup"><span data-stu-id="7382c-156">Specifies the full path of an upgrade package file.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7382c-157">-Profil</span><span class="sxs-lookup"><span data-stu-id="7382c-157">-Profile</span></span>
<span data-ttu-id="7382c-158">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="7382c-158">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7382c-159">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="7382c-159">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7382c-160">-RoleName</span><span class="sxs-lookup"><span data-stu-id="7382c-160">-RoleName</span></span>
<span data-ttu-id="7382c-161">Gibt den Namen der Rolle an, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7382c-161">Specifies the name of the role to upgrade.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7382c-162">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7382c-162">-ServiceName</span></span>
<span data-ttu-id="7382c-163">Gibt den Namen des Azure-Diensts der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="7382c-163">Specifies the name of the Azure service of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7382c-164">-Slot</span><span class="sxs-lookup"><span data-stu-id="7382c-164">-Slot</span></span>
<span data-ttu-id="7382c-165">Gibt die Umgebung der Bereitstellung an, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7382c-165">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="7382c-166">Gültige Werte sind: Production und Staging.</span><span class="sxs-lookup"><span data-stu-id="7382c-166">Valid values are: Production and Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7382c-167">-Status</span><span class="sxs-lookup"><span data-stu-id="7382c-167">-Status</span></span>
<span data-ttu-id="7382c-168">Gibt an, dass mit diesem Cmdlet der Status der Bereitstellung geändert wird.</span><span class="sxs-lookup"><span data-stu-id="7382c-168">Specifies that this cmdlet changes the status of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Status
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7382c-169">-Upgrade</span><span class="sxs-lookup"><span data-stu-id="7382c-169">-Upgrade</span></span>
<span data-ttu-id="7382c-170">Gibt an, dass dieses Cmdlet die Bereitstellung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7382c-170">Specifies that this cmdlet upgrades the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7382c-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7382c-171">CommonParameters</span></span>
<span data-ttu-id="7382c-172">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7382c-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7382c-173">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7382c-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7382c-174">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7382c-174">INPUTS</span></span>

## <span data-ttu-id="7382c-175">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7382c-175">OUTPUTS</span></span>

## <span data-ttu-id="7382c-176">Notizen</span><span class="sxs-lookup"><span data-stu-id="7382c-176">NOTES</span></span>

## <span data-ttu-id="7382c-177">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7382c-177">RELATED LINKS</span></span>

[<span data-ttu-id="7382c-178">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="7382c-178">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="7382c-179">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="7382c-179">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="7382c-180">Verschieben-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="7382c-180">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="7382c-181">Neu – AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="7382c-181">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="7382c-182">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="7382c-182">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="7382c-183">Satz-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="7382c-183">Set-AzureWalkUpgradeDomain</span></span>](./Set-AzureWalkUpgradeDomain.md)


