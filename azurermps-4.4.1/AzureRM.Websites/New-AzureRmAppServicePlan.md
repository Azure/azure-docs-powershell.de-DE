---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
ms.openlocfilehash: e03e7dee6e233934216c04a44c1e100d3e26347b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664707"
---
# <span data-ttu-id="7fa6c-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7fa6c-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="7fa6c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7fa6c-102">SYNOPSIS</span></span>
<span data-ttu-id="7fa6c-103">Erstellt einen Azure App-Service Plan an einem bestimmten Geo-Standort.</span><span class="sxs-lookup"><span data-stu-id="7fa6c-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fa6c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fa6c-104">SYNTAX</span></span>

### <span data-ttu-id="7fa6c-105">S1</span><span class="sxs-lookup"><span data-stu-id="7fa6c-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fa6c-106">S2</span><span class="sxs-lookup"><span data-stu-id="7fa6c-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fa6c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7fa6c-107">DESCRIPTION</span></span>
<span data-ttu-id="7fa6c-108">Mit dem Cmdlet **New-AzureRmAppServicePlan** wird ein Azure App-Dienstplan an einem bestimmten Geo-Standort mit der angegebenen Ebene, der Arbeitsgröße und der Anzahl der Arbeitskräfte erstellt.</span><span class="sxs-lookup"><span data-stu-id="7fa6c-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="7fa6c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7fa6c-109">EXAMPLES</span></span>

### <span data-ttu-id="7fa6c-110">Beispiel 1: Erstellen eines App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="7fa6c-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="7fa6c-111">Dieser Befehl erstellt einen app-Dienstplan mit dem Namen ContosoASP in der Ressourcengruppe Default-Web-westus in Geo-Standort West USA.</span><span class="sxs-lookup"><span data-stu-id="7fa6c-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="7fa6c-112">Der Befehl gibt eine grundlegende Ebene an und ordnet zwei kleine Arbeitskräfte zu.</span><span class="sxs-lookup"><span data-stu-id="7fa6c-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="7fa6c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fa6c-113">PARAMETERS</span></span>

### <span data-ttu-id="7fa6c-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7fa6c-114">-AppServicePlan</span></span>
<span data-ttu-id="7fa6c-115">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="7fa6c-115">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fa6c-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="7fa6c-116">-AseName</span></span>
<span data-ttu-id="7fa6c-117">Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="7fa6c-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="7fa6c-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fa6c-118">-AseResourceGroupName</span></span>
<span data-ttu-id="7fa6c-119">Ressourcengruppen Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="7fa6c-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="7fa6c-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="7fa6c-120">-Location</span></span>
<span data-ttu-id="7fa6c-121">Lage</span><span class="sxs-lookup"><span data-stu-id="7fa6c-121">Location</span></span> 

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

### <span data-ttu-id="7fa6c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7fa6c-122">-Name</span></span>
<span data-ttu-id="7fa6c-123">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="7fa6c-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="7fa6c-124">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="7fa6c-124">-NumberofWorkers</span></span>
<span data-ttu-id="7fa6c-125">Anzahl der Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="7fa6c-125">Number Of Workers</span></span>

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

### <span data-ttu-id="7fa6c-126">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="7fa6c-126">-PerSiteScaling</span></span>
<span data-ttu-id="7fa6c-127">Ob pro Website Skalierung aktiviert werden soll</span><span class="sxs-lookup"><span data-stu-id="7fa6c-127">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="7fa6c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fa6c-128">-ResourceGroupName</span></span>
<span data-ttu-id="7fa6c-129">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="7fa6c-129">Resource Group Name</span></span>

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

### <span data-ttu-id="7fa6c-130">-Tier</span><span class="sxs-lookup"><span data-stu-id="7fa6c-130">-Tier</span></span>
<span data-ttu-id="7fa6c-131">Ebene</span><span class="sxs-lookup"><span data-stu-id="7fa6c-131">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa6c-132">-Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="7fa6c-132">-WorkerSize</span></span>
<span data-ttu-id="7fa6c-133">Größe des Web Worker</span><span class="sxs-lookup"><span data-stu-id="7fa6c-133">Size of web worker</span></span>

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

### <span data-ttu-id="7fa6c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fa6c-134">-DefaultProfile</span></span>
<span data-ttu-id="7fa6c-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7fa6c-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa6c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fa6c-136">CommonParameters</span></span>
<span data-ttu-id="7fa6c-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fa6c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fa6c-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fa6c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fa6c-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7fa6c-139">INPUTS</span></span>

### <span data-ttu-id="7fa6c-140">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="7fa6c-140">ServerFarmWithRichSku</span></span>
<span data-ttu-id="7fa6c-141">Der Parameter "AppServicePlan" akzeptiert den Wert vom Typ "ServerFarmWithRichSku" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7fa6c-141">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="7fa6c-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7fa6c-142">OUTPUTS</span></span>

### <span data-ttu-id="7fa6c-143">Microsoft. Azure. Management. Websites. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="7fa6c-143">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="7fa6c-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="7fa6c-144">NOTES</span></span>

## <span data-ttu-id="7fa6c-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7fa6c-145">RELATED LINKS</span></span>

[<span data-ttu-id="7fa6c-146">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7fa6c-146">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="7fa6c-147">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7fa6c-147">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="7fa6c-148">Satz-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7fa6c-148">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


