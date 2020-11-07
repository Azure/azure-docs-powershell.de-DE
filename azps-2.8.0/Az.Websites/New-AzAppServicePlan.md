---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: 918f590258e6678a66262a6ad2d72a352bf13fd3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826975"
---
# <span data-ttu-id="42d49-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="42d49-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="42d49-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42d49-102">SYNOPSIS</span></span>
<span data-ttu-id="42d49-103">Erstellt einen Azure App-Service Plan an einem bestimmten Geo-Standort.</span><span class="sxs-lookup"><span data-stu-id="42d49-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="42d49-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42d49-104">SYNTAX</span></span>

### <span data-ttu-id="42d49-105">S1</span><span class="sxs-lookup"><span data-stu-id="42d49-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42d49-106">S2</span><span class="sxs-lookup"><span data-stu-id="42d49-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42d49-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42d49-107">DESCRIPTION</span></span>
<span data-ttu-id="42d49-108">Mit dem Cmdlet **New-AzAppServicePlan** wird ein Azure App-Dienstplan an einem bestimmten Geo-Standort mit der angegebenen Ebene, der Arbeitsgröße und der Anzahl der Arbeitskräfte erstellt.</span><span class="sxs-lookup"><span data-stu-id="42d49-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="42d49-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42d49-109">EXAMPLES</span></span>

### <span data-ttu-id="42d49-110">Beispiel 1: Erstellen eines App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="42d49-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="42d49-111">Dieser Befehl erstellt einen app-Dienstplan mit dem Namen ContosoASP in der Ressourcengruppe Default-Web-westus in Geo-Standort West USA.</span><span class="sxs-lookup"><span data-stu-id="42d49-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="42d49-112">Der Befehl gibt eine grundlegende Ebene an und ordnet zwei kleine Arbeitskräfte zu.</span><span class="sxs-lookup"><span data-stu-id="42d49-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="42d49-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="42d49-113">PARAMETERS</span></span>

### <span data-ttu-id="42d49-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="42d49-114">-AppServicePlan</span></span>
<span data-ttu-id="42d49-115">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="42d49-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="42d49-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="42d49-116">-AseName</span></span>
<span data-ttu-id="42d49-117">Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="42d49-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="42d49-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42d49-118">-AseResourceGroupName</span></span>
<span data-ttu-id="42d49-119">Ressourcengruppen Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="42d49-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="42d49-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42d49-120">-AsJob</span></span>
<span data-ttu-id="42d49-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="42d49-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42d49-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d49-122">-DefaultProfile</span></span>
<span data-ttu-id="42d49-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42d49-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42d49-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="42d49-124">-HyperV</span></span>
<span data-ttu-id="42d49-125">Geben Sie dies an, der APP-Service Plan führt Windows-Container aus.</span><span class="sxs-lookup"><span data-stu-id="42d49-125">Specify this, App Service Plan will run Windows Containers</span></span>

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

### <span data-ttu-id="42d49-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="42d49-126">-Location</span></span>
<span data-ttu-id="42d49-127">Lage</span><span class="sxs-lookup"><span data-stu-id="42d49-127">Location</span></span> 

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

### <span data-ttu-id="42d49-128">-Name</span><span class="sxs-lookup"><span data-stu-id="42d49-128">-Name</span></span>
<span data-ttu-id="42d49-129">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="42d49-129">App Service Plan Name</span></span>

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

### <span data-ttu-id="42d49-130">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="42d49-130">-NumberofWorkers</span></span>
<span data-ttu-id="42d49-131">Anzahl der Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="42d49-131">Number Of Workers</span></span>

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

### <span data-ttu-id="42d49-132">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="42d49-132">-PerSiteScaling</span></span>
<span data-ttu-id="42d49-133">Ob pro Website Skalierung aktiviert werden soll</span><span class="sxs-lookup"><span data-stu-id="42d49-133">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="42d49-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42d49-134">-ResourceGroupName</span></span>
<span data-ttu-id="42d49-135">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="42d49-135">Resource Group Name</span></span>

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

### <span data-ttu-id="42d49-136">-Tier</span><span class="sxs-lookup"><span data-stu-id="42d49-136">-Tier</span></span>
<span data-ttu-id="42d49-137">Ebene</span><span class="sxs-lookup"><span data-stu-id="42d49-137">Tier</span></span>

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

### <span data-ttu-id="42d49-138">-Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="42d49-138">-WorkerSize</span></span>
<span data-ttu-id="42d49-139">Größe des Web Worker</span><span class="sxs-lookup"><span data-stu-id="42d49-139">Size of web worker</span></span>

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

### <span data-ttu-id="42d49-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d49-140">CommonParameters</span></span>
<span data-ttu-id="42d49-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42d49-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d49-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42d49-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d49-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42d49-143">INPUTS</span></span>

### <span data-ttu-id="42d49-144">Microsoft. Azure. Commands. webapps. Models. PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="42d49-144">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="42d49-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42d49-145">OUTPUTS</span></span>

### <span data-ttu-id="42d49-146">Microsoft. Azure. Commands. webapps. Models. PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="42d49-146">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="42d49-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="42d49-147">NOTES</span></span>

## <span data-ttu-id="42d49-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42d49-148">RELATED LINKS</span></span>

[<span data-ttu-id="42d49-149">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="42d49-149">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="42d49-150">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="42d49-150">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="42d49-151">Satz-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="42d49-151">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


