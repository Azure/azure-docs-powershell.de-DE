---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: eac153c22a576686feb15b75f3180ed4fb12ec94
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850187"
---
# <span data-ttu-id="12e09-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="12e09-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="12e09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12e09-102">SYNOPSIS</span></span>
<span data-ttu-id="12e09-103">Legt einen Azure-App-Service Plan fest.</span><span class="sxs-lookup"><span data-stu-id="12e09-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12e09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12e09-104">SYNTAX</span></span>

### <span data-ttu-id="12e09-105">S1</span><span class="sxs-lookup"><span data-stu-id="12e09-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12e09-106">S2</span><span class="sxs-lookup"><span data-stu-id="12e09-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <AppServicePlan> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12e09-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12e09-107">DESCRIPTION</span></span>
<span data-ttu-id="12e09-108">Das Cmdlet " **Set-AzureRmAppServicePlan** " legt einen Azure App-Service Plan fest.</span><span class="sxs-lookup"><span data-stu-id="12e09-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="12e09-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12e09-109">EXAMPLES</span></span>

### <span data-ttu-id="12e09-110">1: Ändern eines App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="12e09-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="12e09-111">Mit diesem Befehl wird die PerSiteScaling-Option für den App-Dienstplan mit dem Namen ContosoASP, der zur Ressourcengruppe Default-Web-westus gehört, auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="12e09-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="12e09-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="12e09-112">PARAMETERS</span></span>

### <span data-ttu-id="12e09-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="12e09-113">-AdminSiteName</span></span>
<span data-ttu-id="12e09-114">Name der Administratorwebsite</span><span class="sxs-lookup"><span data-stu-id="12e09-114">Admin Site Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e09-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="12e09-115">-AppServicePlan</span></span>
<span data-ttu-id="12e09-116">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="12e09-116">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12e09-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e09-117">-DefaultProfile</span></span>
<span data-ttu-id="12e09-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="12e09-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e09-119">-Name</span><span class="sxs-lookup"><span data-stu-id="12e09-119">-Name</span></span>
<span data-ttu-id="12e09-120">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="12e09-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e09-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="12e09-121">-NumberofWorkers</span></span>
<span data-ttu-id="12e09-122">Anzahl der Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="12e09-122">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e09-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="12e09-123">-PerSiteScaling</span></span>
<span data-ttu-id="12e09-124">Pro-Site-Skalierungs boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="12e09-124">Per Site Scaling Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e09-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e09-125">-ResourceGroupName</span></span>
<span data-ttu-id="12e09-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="12e09-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e09-127">-Tier</span><span class="sxs-lookup"><span data-stu-id="12e09-127">-Tier</span></span>
<span data-ttu-id="12e09-128">Ebene</span><span class="sxs-lookup"><span data-stu-id="12e09-128">Tier</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e09-129">-Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="12e09-129">-WorkerSize</span></span>
<span data-ttu-id="12e09-130">Workergröße</span><span class="sxs-lookup"><span data-stu-id="12e09-130">Worker Size</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="12e09-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12e09-131">-AsJob</span></span>
<span data-ttu-id="12e09-132">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="12e09-132">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e09-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e09-133">CommonParameters</span></span>
<span data-ttu-id="12e09-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e09-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e09-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12e09-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e09-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12e09-136">INPUTS</span></span>

### <span data-ttu-id="12e09-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="12e09-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="12e09-138">Der Parameter "AppServicePlan" akzeptiert den Wert vom Typ "ServerFarmWithRichSku" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="12e09-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="12e09-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12e09-139">OUTPUTS</span></span>

### <span data-ttu-id="12e09-140">Microsoft. Azure. Management. Websites. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="12e09-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="12e09-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="12e09-141">NOTES</span></span>

## <span data-ttu-id="12e09-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12e09-142">RELATED LINKS</span></span>

[<span data-ttu-id="12e09-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="12e09-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="12e09-144">Neu – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="12e09-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="12e09-145">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="12e09-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="12e09-146">Neustart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="12e09-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="12e09-147">Anfang-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="12e09-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="12e09-148">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="12e09-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


