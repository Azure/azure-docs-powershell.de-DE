---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: af94f1bec48bf54284ccf6e0011753a737dac30b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996542"
---
# <span data-ttu-id="d7190-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d7190-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="d7190-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7190-102">SYNOPSIS</span></span>
<span data-ttu-id="d7190-103">Erstellt einen Azure App-Service Plan an einem bestimmten Geo-Standort.</span><span class="sxs-lookup"><span data-stu-id="d7190-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="d7190-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7190-104">SYNTAX</span></span>

### <span data-ttu-id="d7190-105">S1</span><span class="sxs-lookup"><span data-stu-id="d7190-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7190-106">S2</span><span class="sxs-lookup"><span data-stu-id="d7190-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7190-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7190-107">DESCRIPTION</span></span>
<span data-ttu-id="d7190-108">Mit dem Cmdlet **New-AzAppServicePlan** wird ein Azure App-Dienstplan an einem bestimmten Geo-Standort mit der angegebenen Ebene, der Arbeitsgröße und der Anzahl der Arbeitskräfte erstellt.</span><span class="sxs-lookup"><span data-stu-id="d7190-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="d7190-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7190-109">EXAMPLES</span></span>

### <span data-ttu-id="d7190-110">Beispiel 1: Erstellen eines App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="d7190-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="d7190-111">Dieser Befehl erstellt einen app-Dienstplan mit dem Namen ContosoASP in der Ressourcengruppe Default-Web-westus in Geo-Standort West USA.</span><span class="sxs-lookup"><span data-stu-id="d7190-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="d7190-112">Der Befehl gibt eine grundlegende Ebene an und ordnet zwei kleine Arbeitskräfte zu.</span><span class="sxs-lookup"><span data-stu-id="d7190-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="d7190-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7190-113">PARAMETERS</span></span>

### <span data-ttu-id="d7190-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d7190-114">-AppServicePlan</span></span>
<span data-ttu-id="d7190-115">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="d7190-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="d7190-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="d7190-116">-AseName</span></span>
<span data-ttu-id="d7190-117">Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="d7190-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="d7190-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7190-118">-AseResourceGroupName</span></span>
<span data-ttu-id="d7190-119">Ressourcengruppen Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="d7190-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="d7190-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7190-120">-AsJob</span></span>
<span data-ttu-id="d7190-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d7190-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7190-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7190-122">-DefaultProfile</span></span>
<span data-ttu-id="d7190-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7190-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7190-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="d7190-124">-HyperV</span></span>
<span data-ttu-id="d7190-125">Geben Sie dies an, der APP-Service Plan führt Windows-Container aus.</span><span class="sxs-lookup"><span data-stu-id="d7190-125">Specify this, App Service Plan will run Windows Containers</span></span>

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

### <span data-ttu-id="d7190-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="d7190-126">-Location</span></span>
<span data-ttu-id="d7190-127">Lage</span><span class="sxs-lookup"><span data-stu-id="d7190-127">Location</span></span> 

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

### <span data-ttu-id="d7190-128">-Name</span><span class="sxs-lookup"><span data-stu-id="d7190-128">-Name</span></span>
<span data-ttu-id="d7190-129">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="d7190-129">App Service Plan Name</span></span>

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

### <span data-ttu-id="d7190-130">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="d7190-130">-NumberofWorkers</span></span>
<span data-ttu-id="d7190-131">Anzahl der Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="d7190-131">Number Of Workers</span></span>

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

### <span data-ttu-id="d7190-132">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="d7190-132">-PerSiteScaling</span></span>
<span data-ttu-id="d7190-133">Ob pro Website Skalierung aktiviert werden soll</span><span class="sxs-lookup"><span data-stu-id="d7190-133">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="d7190-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7190-134">-ResourceGroupName</span></span>
<span data-ttu-id="d7190-135">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="d7190-135">Resource Group Name</span></span>

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

### <span data-ttu-id="d7190-136">-Tier</span><span class="sxs-lookup"><span data-stu-id="d7190-136">-Tier</span></span>
<span data-ttu-id="d7190-137">Ebene</span><span class="sxs-lookup"><span data-stu-id="d7190-137">Tier</span></span>

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

### <span data-ttu-id="d7190-138">-Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="d7190-138">-WorkerSize</span></span>
<span data-ttu-id="d7190-139">Größe des Web Worker</span><span class="sxs-lookup"><span data-stu-id="d7190-139">Size of web worker</span></span>

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

### <span data-ttu-id="d7190-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7190-140">CommonParameters</span></span>
<span data-ttu-id="d7190-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7190-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7190-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7190-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7190-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7190-143">INPUTS</span></span>

### <span data-ttu-id="d7190-144">Microsoft. Azure. Commands. webapps. Models. PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="d7190-144">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="d7190-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7190-145">OUTPUTS</span></span>

### <span data-ttu-id="d7190-146">Microsoft. Azure. Commands. webapps. Models. PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="d7190-146">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="d7190-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7190-147">NOTES</span></span>

## <span data-ttu-id="d7190-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7190-148">RELATED LINKS</span></span>

[<span data-ttu-id="d7190-149">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d7190-149">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="d7190-150">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d7190-150">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="d7190-151">Satz-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d7190-151">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


