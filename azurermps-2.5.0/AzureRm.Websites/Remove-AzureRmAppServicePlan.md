---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: e8ce0397a59a72e2960a8e0af978c1b5484c53af
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848063"
---
# <span data-ttu-id="472c3-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="472c3-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="472c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="472c3-102">SYNOPSIS</span></span>
<span data-ttu-id="472c3-103">Entfernt einen Azure App-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="472c3-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="472c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="472c3-104">SYNTAX</span></span>

### <span data-ttu-id="472c3-105">S1</span><span class="sxs-lookup"><span data-stu-id="472c3-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="472c3-106">S2</span><span class="sxs-lookup"><span data-stu-id="472c3-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <AppServicePlan> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="472c3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="472c3-107">DESCRIPTION</span></span>
<span data-ttu-id="472c3-108">Das Cmdlet **Remove-AzureRmAppServicePlan** entfernt einen Azure App-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="472c3-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="472c3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="472c3-109">EXAMPLES</span></span>

### <span data-ttu-id="472c3-110">Beispiel 1: Entfernen eines App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="472c3-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="472c3-111">Mit diesem Befehl wird der Azure App-Service Plan mit dem Namen ContosoASP entfernt, der zur Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="472c3-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="472c3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="472c3-112">PARAMETERS</span></span>

### <span data-ttu-id="472c3-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="472c3-113">-AppServicePlan</span></span>
<span data-ttu-id="472c3-114">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="472c3-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="472c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="472c3-115">-DefaultProfile</span></span>
<span data-ttu-id="472c3-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="472c3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="472c3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="472c3-117">-Force</span></span>
<span data-ttu-id="472c3-118">Option "gewaltsam entfernen"</span><span class="sxs-lookup"><span data-stu-id="472c3-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="472c3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="472c3-119">-Name</span></span>
<span data-ttu-id="472c3-120">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="472c3-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="472c3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="472c3-121">-ResourceGroupName</span></span>
<span data-ttu-id="472c3-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="472c3-122">Resource Group Name</span></span>

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

### <span data-ttu-id="472c3-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="472c3-123">-Confirm</span></span>
<span data-ttu-id="472c3-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="472c3-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="472c3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="472c3-125">-WhatIf</span></span>
<span data-ttu-id="472c3-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="472c3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="472c3-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="472c3-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="472c3-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="472c3-128">-AsJob</span></span>
<span data-ttu-id="472c3-129">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="472c3-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="472c3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="472c3-130">CommonParameters</span></span>
<span data-ttu-id="472c3-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="472c3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="472c3-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="472c3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="472c3-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="472c3-133">INPUTS</span></span>

### <span data-ttu-id="472c3-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="472c3-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="472c3-135">Der Parameter "AppServicePlan" akzeptiert den Wert vom Typ "ServerFarmWithRichSku" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="472c3-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="472c3-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="472c3-136">OUTPUTS</span></span>

### <span data-ttu-id="472c3-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="472c3-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="472c3-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="472c3-138">NOTES</span></span>

## <span data-ttu-id="472c3-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="472c3-139">RELATED LINKS</span></span>

[<span data-ttu-id="472c3-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="472c3-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="472c3-141">Neu – AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="472c3-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="472c3-142">Satz-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="472c3-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


