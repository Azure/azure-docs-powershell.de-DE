---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: 9a1c1de8aef41089cfc874cf35b26fcc9bf0be52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948179"
---
# <span data-ttu-id="ccf9d-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ccf9d-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="ccf9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccf9d-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf9d-103">Erstellt einen Azure App Service-Plan an einem bestimmten Geospeicherort.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="ccf9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ccf9d-104">SYNTAX</span></span>

### <span data-ttu-id="ccf9d-105">S1</span><span class="sxs-lookup"><span data-stu-id="ccf9d-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-Tag <Hashtable>] [-Linux] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccf9d-106">S2</span><span class="sxs-lookup"><span data-stu-id="ccf9d-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccf9d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ccf9d-107">DESCRIPTION</span></span>
<span data-ttu-id="ccf9d-108">Das **Cmdlet New-AzAppServicePlan** erstellt einen Azure App Service-Plan an einem bestimmten Geo-Speicherort mit der angegebenen Ebene, Der Größe der Mitarbeiter und der Anzahl der Arbeitskräfte.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="ccf9d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ccf9d-109">EXAMPLES</span></span>

### <span data-ttu-id="ccf9d-110">Beispiel 1: Erstellen eines App Service-Plans</span><span class="sxs-lookup"><span data-stu-id="ccf9d-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="ccf9d-111">Mit diesem Befehl wird ein App Service-Plan namens ContosoASP in der Ressourcengruppe "Default-Web-WestUS" im Geospeicherort West US erstellt.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="ccf9d-112">Der Befehl gibt eine Einfache Ebene an und weist zwei kleine Arbeitskräfte zu.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="ccf9d-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ccf9d-113">PARAMETERS</span></span>

### <span data-ttu-id="ccf9d-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ccf9d-114">-AppServicePlan</span></span>
<span data-ttu-id="ccf9d-115">App Service Plan Object</span><span class="sxs-lookup"><span data-stu-id="ccf9d-115">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf9d-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="ccf9d-116">-AseName</span></span>
<span data-ttu-id="ccf9d-117">Name der App-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="ccf9d-117">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf9d-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccf9d-118">-AseResourceGroupName</span></span>
<span data-ttu-id="ccf9d-119">Gruppenname der Ressourcengruppe "App Service Environment"</span><span class="sxs-lookup"><span data-stu-id="ccf9d-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf9d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccf9d-120">-AsJob</span></span>
<span data-ttu-id="ccf9d-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ccf9d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccf9d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf9d-122">-DefaultProfile</span></span>
<span data-ttu-id="ccf9d-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccf9d-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="ccf9d-124">-HyperV</span></span>
<span data-ttu-id="ccf9d-125">Geben Sie dies an, im App-Dienstplan werden Windows-Container ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-125">Specify this, App Service Plan will run Windows Containers</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf9d-126">-Linux</span><span class="sxs-lookup"><span data-stu-id="ccf9d-126">-Linux</span></span>
<span data-ttu-id="ccf9d-127">Geben Sie dies an, im App Service Plan werden Linux-Container ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-127">Specify this, App Service Plan will run Linux Containers</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf9d-128">-Location</span><span class="sxs-lookup"><span data-stu-id="ccf9d-128">-Location</span></span>
<span data-ttu-id="ccf9d-129">Ort</span><span class="sxs-lookup"><span data-stu-id="ccf9d-129">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf9d-130">-Name</span><span class="sxs-lookup"><span data-stu-id="ccf9d-130">-Name</span></span>
<span data-ttu-id="ccf9d-131">Name des App-Dienstplans</span><span class="sxs-lookup"><span data-stu-id="ccf9d-131">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf9d-132">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="ccf9d-132">-NumberofWorkers</span></span>
<span data-ttu-id="ccf9d-133">Anzahl der Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="ccf9d-133">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf9d-134">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="ccf9d-134">-PerSiteScaling</span></span>
<span data-ttu-id="ccf9d-135">Aktivieren der Skalierung pro Website</span><span class="sxs-lookup"><span data-stu-id="ccf9d-135">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf9d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccf9d-136">-ResourceGroupName</span></span>
<span data-ttu-id="ccf9d-137">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="ccf9d-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf9d-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="ccf9d-138">-Tag</span></span>
<span data-ttu-id="ccf9d-139">Tags sind Namens-/Wertpaare, mit denen Sie Ressourcen kategorisieren können</span><span class="sxs-lookup"><span data-stu-id="ccf9d-139">Tags are name/value pairs that enable you to categorize resources</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf9d-140">-Tier</span><span class="sxs-lookup"><span data-stu-id="ccf9d-140">-Tier</span></span>
<span data-ttu-id="ccf9d-141">Stufe</span><span class="sxs-lookup"><span data-stu-id="ccf9d-141">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf9d-142">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="ccf9d-142">-WorkerSize</span></span>
<span data-ttu-id="ccf9d-143">Größe des Webworkers</span><span class="sxs-lookup"><span data-stu-id="ccf9d-143">Size of web worker</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf9d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf9d-144">CommonParameters</span></span>
<span data-ttu-id="ccf9d-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf9d-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccf9d-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf9d-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ccf9d-147">INPUTS</span></span>

### <span data-ttu-id="ccf9d-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ccf9d-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="ccf9d-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ccf9d-149">OUTPUTS</span></span>

### <span data-ttu-id="ccf9d-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ccf9d-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="ccf9d-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ccf9d-151">NOTES</span></span>

## <span data-ttu-id="ccf9d-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ccf9d-152">RELATED LINKS</span></span>

[<span data-ttu-id="ccf9d-153">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ccf9d-153">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="ccf9d-154">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ccf9d-154">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="ccf9d-155">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ccf9d-155">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


