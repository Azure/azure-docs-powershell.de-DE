---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 2228eb7562ed7a0ffa1c0098086c085985e45fee
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367098"
---
# <span data-ttu-id="f53ef-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f53ef-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="f53ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f53ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f53ef-103">Erstellt einen Azure Web App-Slot.</span><span class="sxs-lookup"><span data-stu-id="f53ef-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="f53ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f53ef-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f53ef-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f53ef-105">DESCRIPTION</span></span>
<span data-ttu-id="f53ef-106">Das **Cmdlet "New-AzWebAppSlot"** erstellt eine Azure Web App-Slot in einer bestimmten Ressourcengruppe, die den angegebenen App Service Plan und das Rechenzentrum verwendet.</span><span class="sxs-lookup"><span data-stu-id="f53ef-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="f53ef-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f53ef-107">EXAMPLES</span></span>

### <span data-ttu-id="f53ef-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f53ef-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="f53ef-109">Mit diesem Befehl wird ein Slot mit dem Namen "Slot001" unter einer vorhandenen Web App namens "ContosoSite" in der vorhandenen Ressourcengruppe "Default-Web-WestUS" im Rechenzentrum "USA, Westen" erstellt.</span><span class="sxs-lookup"><span data-stu-id="f53ef-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="f53ef-110">Der Befehl verwendet einen vorhandenen App -Dienstplan namens "ContosoServicePlan".</span><span class="sxs-lookup"><span data-stu-id="f53ef-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="f53ef-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f53ef-111">PARAMETERS</span></span>

### <span data-ttu-id="f53ef-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f53ef-112">-AppServicePlan</span></span>
<span data-ttu-id="f53ef-113">Name des App-Serviceplans oder Id des App-Serviceplans. Wenn sich das Slot und der Plan für den App-Dienst in verschiedenen Ressourcengruppen befinden, verwenden Sie die ID anstelle des Namens.</span><span class="sxs-lookup"><span data-stu-id="f53ef-113">App Service Plan Name or App Service Plan Id. If the Slot and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="f53ef-114">Die Plan-ID der App kann mit: $asp = Get-AzAppServicePlan -ResourceGroup myRG -Name MyWebapp $asp.id wird die Id des App-Serviceplans zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f53ef-114">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53ef-115">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="f53ef-115">-AppSettingsOverrides</span></span>
<span data-ttu-id="f53ef-116">#A0 setzt Hashtable außer Kraft</span><span class="sxs-lookup"><span data-stu-id="f53ef-116">App Settings Overrides Hashtable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53ef-117">-AseName</span><span class="sxs-lookup"><span data-stu-id="f53ef-117">-AseName</span></span>
<span data-ttu-id="f53ef-118">Name der App-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="f53ef-118">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53ef-119">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f53ef-119">-AseResourceGroupName</span></span>
<span data-ttu-id="f53ef-120">Ressourcengruppenname der App-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="f53ef-120">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53ef-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f53ef-121">-AsJob</span></span>
<span data-ttu-id="f53ef-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f53ef-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53ef-123">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="f53ef-123">-ContainerImageName</span></span>
<span data-ttu-id="f53ef-124">Container Image Name and optional tag, for example (image:tag)</span><span class="sxs-lookup"><span data-stu-id="f53ef-124">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53ef-125">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="f53ef-125">-ContainerRegistryPassword</span></span>
<span data-ttu-id="f53ef-126">Private Container Registry Password</span><span class="sxs-lookup"><span data-stu-id="f53ef-126">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53ef-127">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="f53ef-127">-ContainerRegistryUrl</span></span>
<span data-ttu-id="f53ef-128">URL des Registrierungsservers für privaten Container</span><span class="sxs-lookup"><span data-stu-id="f53ef-128">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53ef-129">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="f53ef-129">-ContainerRegistryUser</span></span>
<span data-ttu-id="f53ef-130">Private Container Registry Username</span><span class="sxs-lookup"><span data-stu-id="f53ef-130">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53ef-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f53ef-131">-DefaultProfile</span></span>
<span data-ttu-id="f53ef-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f53ef-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f53ef-133">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="f53ef-133">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="f53ef-134">Aktiviert/Deaktiviert den Container-Webhook für die fortlaufende Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="f53ef-134">Enables/Disables container continuous deployment webhook</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53ef-135">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="f53ef-135">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="f53ef-136">Option "Benutzerdefinierte Hostnamen ignorieren"</span><span class="sxs-lookup"><span data-stu-id="f53ef-136">Ignore Custom HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53ef-137">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="f53ef-137">-IgnoreSourceControl</span></span>
<span data-ttu-id="f53ef-138">Option "Quellcodeverwaltung ignorieren"</span><span class="sxs-lookup"><span data-stu-id="f53ef-138">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53ef-139">-Name</span><span class="sxs-lookup"><span data-stu-id="f53ef-139">-Name</span></span>
<span data-ttu-id="f53ef-140">Webapp Name</span><span class="sxs-lookup"><span data-stu-id="f53ef-140">Webapp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f53ef-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f53ef-141">-ResourceGroupName</span></span>
<span data-ttu-id="f53ef-142">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f53ef-142">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53ef-143">-Slot</span><span class="sxs-lookup"><span data-stu-id="f53ef-143">-Slot</span></span>
<span data-ttu-id="f53ef-144">Name des Webapp-Slot</span><span class="sxs-lookup"><span data-stu-id="f53ef-144">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53ef-145">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="f53ef-145">-SourceWebApp</span></span>
<span data-ttu-id="f53ef-146">Quell-WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="f53ef-146">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f53ef-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f53ef-147">CommonParameters</span></span>
<span data-ttu-id="f53ef-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f53ef-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f53ef-149">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f53ef-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f53ef-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f53ef-150">INPUTS</span></span>

### <span data-ttu-id="f53ef-151">System.String</span><span class="sxs-lookup"><span data-stu-id="f53ef-151">System.String</span></span>

### <span data-ttu-id="f53ef-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f53ef-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f53ef-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f53ef-153">OUTPUTS</span></span>

### <span data-ttu-id="f53ef-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f53ef-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f53ef-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f53ef-155">NOTES</span></span>

## <span data-ttu-id="f53ef-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f53ef-156">RELATED LINKS</span></span>

[<span data-ttu-id="f53ef-157">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f53ef-157">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="f53ef-158">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f53ef-158">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="f53ef-159">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f53ef-159">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="f53ef-160">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f53ef-160">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="f53ef-161">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f53ef-161">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="f53ef-162">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f53ef-162">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="f53ef-163">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f53ef-163">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="f53ef-164">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f53ef-164">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
