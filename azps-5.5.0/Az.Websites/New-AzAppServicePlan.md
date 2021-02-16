---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: 863a1b42a6decd6b979516d21c007a9626e36d23
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173401"
---
# <span data-ttu-id="25f56-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="25f56-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="25f56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25f56-102">SYNOPSIS</span></span>
<span data-ttu-id="25f56-103">Erstellt einen Azure App Service Plan an einem bestimmten Geo-Standort.</span><span class="sxs-lookup"><span data-stu-id="25f56-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="25f56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25f56-104">SYNTAX</span></span>

### <span data-ttu-id="25f56-105">S1</span><span class="sxs-lookup"><span data-stu-id="25f56-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-Tag <Hashtable>] [-Linux] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25f56-106">S2</span><span class="sxs-lookup"><span data-stu-id="25f56-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25f56-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25f56-107">DESCRIPTION</span></span>
<span data-ttu-id="25f56-108">Das **Cmdlet "New-AzAppServicePlan"** erstellt einen Azure App Service Plan an einer bestimmten Geoposition mit der angegebenen Stufe, Workergröße und Anzahl der Arbeitskräfte.</span><span class="sxs-lookup"><span data-stu-id="25f56-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="25f56-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="25f56-109">EXAMPLES</span></span>

### <span data-ttu-id="25f56-110">Beispiel 1: Erstellen eines App -Dienstplans</span><span class="sxs-lookup"><span data-stu-id="25f56-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="25f56-111">Mit diesem Befehl wird ein App-Service-Plan namens "ContosoASP" in der Ressourcengruppe "Default-Web-WestUS" im Geospeicherort "USA" erstellt.</span><span class="sxs-lookup"><span data-stu-id="25f56-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="25f56-112">Der Befehl gibt eine einfache Stufe an und weist zwei kleine Arbeitskräfte zu.</span><span class="sxs-lookup"><span data-stu-id="25f56-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="25f56-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25f56-113">PARAMETERS</span></span>

### <span data-ttu-id="25f56-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="25f56-114">-AppServicePlan</span></span>
<span data-ttu-id="25f56-115">App Service Plan Object</span><span class="sxs-lookup"><span data-stu-id="25f56-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="25f56-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="25f56-116">-AseName</span></span>
<span data-ttu-id="25f56-117">Name der App-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="25f56-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="25f56-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25f56-118">-AseResourceGroupName</span></span>
<span data-ttu-id="25f56-119">Ressourcengruppenname der App-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="25f56-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="25f56-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25f56-120">-AsJob</span></span>
<span data-ttu-id="25f56-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="25f56-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25f56-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25f56-122">-DefaultProfile</span></span>
<span data-ttu-id="25f56-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25f56-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25f56-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="25f56-124">-HyperV</span></span>
<span data-ttu-id="25f56-125">Geben Sie dies an, mit dem Plan für den App-Dienst werden windows-Container ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25f56-125">Specify this, App Service Plan will run Windows Containers</span></span>

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

### <span data-ttu-id="25f56-126">-Linux</span><span class="sxs-lookup"><span data-stu-id="25f56-126">-Linux</span></span>
<span data-ttu-id="25f56-127">Geben Sie dies an, mit dem App-Serviceplan werden die Linux Container ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25f56-127">Specify this, App Service Plan will run Linux Containers</span></span>

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

### <span data-ttu-id="25f56-128">-Location</span><span class="sxs-lookup"><span data-stu-id="25f56-128">-Location</span></span>
<span data-ttu-id="25f56-129">Position</span><span class="sxs-lookup"><span data-stu-id="25f56-129">Location</span></span> 

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

### <span data-ttu-id="25f56-130">-Name</span><span class="sxs-lookup"><span data-stu-id="25f56-130">-Name</span></span>
<span data-ttu-id="25f56-131">Name des App-Serviceplans</span><span class="sxs-lookup"><span data-stu-id="25f56-131">App Service Plan Name</span></span>

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

### <span data-ttu-id="25f56-132">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="25f56-132">-NumberofWorkers</span></span>
<span data-ttu-id="25f56-133">Anzahl der Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="25f56-133">Number Of Workers</span></span>

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

### <span data-ttu-id="25f56-134">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="25f56-134">-PerSiteScaling</span></span>
<span data-ttu-id="25f56-135">Aktivieren der Skalierung pro Standort</span><span class="sxs-lookup"><span data-stu-id="25f56-135">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="25f56-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25f56-136">-ResourceGroupName</span></span>
<span data-ttu-id="25f56-137">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="25f56-137">Resource Group Name</span></span>

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

### <span data-ttu-id="25f56-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="25f56-138">-Tag</span></span>
<span data-ttu-id="25f56-139">Tags sind Name/Wert-Paare, mit denen Sie Ressourcen kategorisieren können.</span><span class="sxs-lookup"><span data-stu-id="25f56-139">Tags are name/value pairs that enable you to categorize resources</span></span>

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

### <span data-ttu-id="25f56-140">-Tier</span><span class="sxs-lookup"><span data-stu-id="25f56-140">-Tier</span></span>
<span data-ttu-id="25f56-141">Stufe</span><span class="sxs-lookup"><span data-stu-id="25f56-141">Tier</span></span>

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

### <span data-ttu-id="25f56-142">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="25f56-142">-WorkerSize</span></span>
<span data-ttu-id="25f56-143">Größe des Webworkers</span><span class="sxs-lookup"><span data-stu-id="25f56-143">Size of web worker</span></span>

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

### <span data-ttu-id="25f56-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25f56-144">CommonParameters</span></span>
<span data-ttu-id="25f56-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25f56-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25f56-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25f56-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25f56-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="25f56-147">INPUTS</span></span>

### <span data-ttu-id="25f56-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="25f56-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="25f56-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="25f56-149">OUTPUTS</span></span>

### <span data-ttu-id="25f56-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="25f56-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="25f56-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="25f56-151">NOTES</span></span>

## <span data-ttu-id="25f56-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="25f56-152">RELATED LINKS</span></span>

[<span data-ttu-id="25f56-153">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="25f56-153">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="25f56-154">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="25f56-154">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="25f56-155">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="25f56-155">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


