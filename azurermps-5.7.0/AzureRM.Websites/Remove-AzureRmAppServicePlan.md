---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: d5164e47dd759538fea6f0ab143ef9640055f1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480721"
---
# <span data-ttu-id="1ae59-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1ae59-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="1ae59-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1ae59-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae59-103">Entfernt einen Azure App-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="1ae59-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ae59-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ae59-104">SYNTAX</span></span>

### <span data-ttu-id="1ae59-105">S1</span><span class="sxs-lookup"><span data-stu-id="1ae59-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae59-106">S2</span><span class="sxs-lookup"><span data-stu-id="1ae59-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ae59-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ae59-107">DESCRIPTION</span></span>
<span data-ttu-id="1ae59-108">Das Cmdlet **Remove-AzureRmAppServicePlan** entfernt einen Azure App-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="1ae59-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="1ae59-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ae59-109">EXAMPLES</span></span>

### <span data-ttu-id="1ae59-110">Beispiel 1: Entfernen eines App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="1ae59-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="1ae59-111">Mit diesem Befehl wird der Azure App-Service Plan mit dem Namen ContosoASP entfernt, der zur Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="1ae59-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="1ae59-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ae59-112">PARAMETERS</span></span>

### <span data-ttu-id="1ae59-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1ae59-113">-AppServicePlan</span></span>
<span data-ttu-id="1ae59-114">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="1ae59-114">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae59-115">-DefaultProfile</span></span>
<span data-ttu-id="1ae59-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1ae59-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ae59-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1ae59-117">-Force</span></span>
<span data-ttu-id="1ae59-118">Option "gewaltsam entfernen"</span><span class="sxs-lookup"><span data-stu-id="1ae59-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="1ae59-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1ae59-119">-Name</span></span>
<span data-ttu-id="1ae59-120">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="1ae59-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="1ae59-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae59-121">-ResourceGroupName</span></span>
<span data-ttu-id="1ae59-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="1ae59-122">Resource Group Name</span></span>

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

### <span data-ttu-id="1ae59-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ae59-123">-Confirm</span></span>
<span data-ttu-id="1ae59-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ae59-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ae59-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ae59-125">-WhatIf</span></span>
<span data-ttu-id="1ae59-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ae59-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ae59-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ae59-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ae59-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ae59-128">-AsJob</span></span>
<span data-ttu-id="1ae59-129">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1ae59-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ae59-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae59-130">CommonParameters</span></span>
<span data-ttu-id="1ae59-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae59-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae59-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae59-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae59-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ae59-133">INPUTS</span></span>

### <span data-ttu-id="1ae59-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="1ae59-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="1ae59-135">Der Parameter "AppServicePlan" akzeptiert den Wert vom Typ "ServerFarmWithRichSku" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1ae59-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="1ae59-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1ae59-136">OUTPUTS</span></span>

### <span data-ttu-id="1ae59-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1ae59-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="1ae59-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ae59-138">NOTES</span></span>

## <span data-ttu-id="1ae59-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1ae59-139">RELATED LINKS</span></span>

[<span data-ttu-id="1ae59-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1ae59-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="1ae59-141">Neu – AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1ae59-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="1ae59-142">Satz-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1ae59-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


