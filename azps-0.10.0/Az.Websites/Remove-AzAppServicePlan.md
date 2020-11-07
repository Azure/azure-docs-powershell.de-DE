---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: 3d0e3ad30df71700eb83938181ed86a97a77528a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842723"
---
# <span data-ttu-id="bd78a-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bd78a-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="bd78a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bd78a-102">SYNOPSIS</span></span>
<span data-ttu-id="bd78a-103">Entfernt einen Azure App-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="bd78a-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="bd78a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd78a-104">SYNTAX</span></span>

### <span data-ttu-id="bd78a-105">S1</span><span class="sxs-lookup"><span data-stu-id="bd78a-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd78a-106">S2</span><span class="sxs-lookup"><span data-stu-id="bd78a-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AppServicePlan] <AppServicePlan> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd78a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd78a-107">DESCRIPTION</span></span>
<span data-ttu-id="bd78a-108">Das Cmdlet **Remove-AzAppServicePlan** entfernt einen Azure App-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="bd78a-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="bd78a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd78a-109">EXAMPLES</span></span>

### <span data-ttu-id="bd78a-110">Beispiel 1: Entfernen eines App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="bd78a-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="bd78a-111">Mit diesem Befehl wird der Azure App-Service Plan mit dem Namen ContosoASP entfernt, der zur Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="bd78a-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="bd78a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd78a-112">PARAMETERS</span></span>

### <span data-ttu-id="bd78a-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bd78a-113">-AppServicePlan</span></span>
<span data-ttu-id="bd78a-114">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="bd78a-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="bd78a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd78a-115">-DefaultProfile</span></span>
<span data-ttu-id="bd78a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bd78a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd78a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bd78a-117">-Force</span></span>
<span data-ttu-id="bd78a-118">Option "gewaltsam entfernen"</span><span class="sxs-lookup"><span data-stu-id="bd78a-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="bd78a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bd78a-119">-Name</span></span>
<span data-ttu-id="bd78a-120">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="bd78a-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="bd78a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd78a-121">-ResourceGroupName</span></span>
<span data-ttu-id="bd78a-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="bd78a-122">Resource Group Name</span></span>

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

### <span data-ttu-id="bd78a-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bd78a-123">-Confirm</span></span>
<span data-ttu-id="bd78a-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bd78a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd78a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd78a-125">-WhatIf</span></span>
<span data-ttu-id="bd78a-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bd78a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd78a-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd78a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd78a-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd78a-128">-AsJob</span></span>
<span data-ttu-id="bd78a-129">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="bd78a-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd78a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd78a-130">CommonParameters</span></span>
<span data-ttu-id="bd78a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd78a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd78a-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd78a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd78a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bd78a-133">INPUTS</span></span>

### <span data-ttu-id="bd78a-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="bd78a-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="bd78a-135">Der Parameter "AppServicePlan" akzeptiert den Wert vom Typ "ServerFarmWithRichSku" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bd78a-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="bd78a-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bd78a-136">OUTPUTS</span></span>

### <span data-ttu-id="bd78a-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bd78a-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="bd78a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="bd78a-138">NOTES</span></span>

## <span data-ttu-id="bd78a-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bd78a-139">RELATED LINKS</span></span>

[<span data-ttu-id="bd78a-140">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bd78a-140">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="bd78a-141">Neu – AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bd78a-141">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="bd78a-142">Satz-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bd78a-142">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


