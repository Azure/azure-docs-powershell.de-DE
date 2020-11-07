---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: b679b98e84f389e35e7dc291822049e554d40a9a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842680"
---
# <span data-ttu-id="689c5-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="689c5-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="689c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="689c5-102">SYNOPSIS</span></span>
<span data-ttu-id="689c5-103">Legt einen Azure-App-Service Plan fest.</span><span class="sxs-lookup"><span data-stu-id="689c5-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="689c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="689c5-104">SYNTAX</span></span>

### <span data-ttu-id="689c5-105">S1</span><span class="sxs-lookup"><span data-stu-id="689c5-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="689c5-106">S2</span><span class="sxs-lookup"><span data-stu-id="689c5-106">S2</span></span>
```
Set-AzAppServicePlan [-AppServicePlan] <AppServicePlan> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="689c5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="689c5-107">DESCRIPTION</span></span>
<span data-ttu-id="689c5-108">Das Cmdlet " **Set-AzAppServicePlan** " legt einen Azure App-Service Plan fest.</span><span class="sxs-lookup"><span data-stu-id="689c5-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="689c5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="689c5-109">EXAMPLES</span></span>

### <span data-ttu-id="689c5-110">1: Ändern eines App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="689c5-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="689c5-111">Mit diesem Befehl wird die PerSiteScaling-Option für den App-Dienstplan mit dem Namen ContosoASP, der zur Ressourcengruppe Default-Web-westus gehört, auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="689c5-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="689c5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="689c5-112">PARAMETERS</span></span>

### <span data-ttu-id="689c5-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="689c5-113">-AdminSiteName</span></span>
<span data-ttu-id="689c5-114">Name der Administratorwebsite</span><span class="sxs-lookup"><span data-stu-id="689c5-114">Admin Site Name</span></span>

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

### <span data-ttu-id="689c5-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="689c5-115">-AppServicePlan</span></span>
<span data-ttu-id="689c5-116">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="689c5-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="689c5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="689c5-117">-DefaultProfile</span></span>
<span data-ttu-id="689c5-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="689c5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689c5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="689c5-119">-Name</span></span>
<span data-ttu-id="689c5-120">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="689c5-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="689c5-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="689c5-121">-NumberofWorkers</span></span>
<span data-ttu-id="689c5-122">Anzahl der Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="689c5-122">Number Of Workers</span></span>

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

### <span data-ttu-id="689c5-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="689c5-123">-PerSiteScaling</span></span>
<span data-ttu-id="689c5-124">Pro-Site-Skalierungs boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="689c5-124">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="689c5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="689c5-125">-ResourceGroupName</span></span>
<span data-ttu-id="689c5-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="689c5-126">Resource Group Name</span></span>

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

### <span data-ttu-id="689c5-127">-Tier</span><span class="sxs-lookup"><span data-stu-id="689c5-127">-Tier</span></span>
<span data-ttu-id="689c5-128">Ebene</span><span class="sxs-lookup"><span data-stu-id="689c5-128">Tier</span></span>

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

### <span data-ttu-id="689c5-129">-Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="689c5-129">-WorkerSize</span></span>
<span data-ttu-id="689c5-130">Workergröße</span><span class="sxs-lookup"><span data-stu-id="689c5-130">Worker Size</span></span>

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
### <span data-ttu-id="689c5-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="689c5-131">-AsJob</span></span>
<span data-ttu-id="689c5-132">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="689c5-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="689c5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="689c5-133">CommonParameters</span></span>
<span data-ttu-id="689c5-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="689c5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="689c5-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="689c5-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="689c5-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="689c5-136">INPUTS</span></span>

### <span data-ttu-id="689c5-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="689c5-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="689c5-138">Der Parameter "AppServicePlan" akzeptiert den Wert vom Typ "ServerFarmWithRichSku" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="689c5-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="689c5-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="689c5-139">OUTPUTS</span></span>

### <span data-ttu-id="689c5-140">Microsoft. Azure. Management. Websites. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="689c5-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="689c5-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="689c5-141">NOTES</span></span>

## <span data-ttu-id="689c5-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="689c5-142">RELATED LINKS</span></span>

[<span data-ttu-id="689c5-143">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="689c5-143">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="689c5-144">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="689c5-144">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="689c5-145">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="689c5-145">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="689c5-146">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="689c5-146">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="689c5-147">Anfang-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="689c5-147">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="689c5-148">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="689c5-148">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


