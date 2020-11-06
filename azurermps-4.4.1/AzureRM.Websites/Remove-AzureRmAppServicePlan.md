---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: d1d07e27a7ad6fb6059cbfc8e4c972b1cedaf7e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504666"
---
# <span data-ttu-id="2fc72-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2fc72-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="2fc72-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2fc72-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc72-103">Entfernt einen Azure App-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="2fc72-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fc72-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fc72-104">SYNTAX</span></span>

### <span data-ttu-id="2fc72-105">S1</span><span class="sxs-lookup"><span data-stu-id="2fc72-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc72-106">S2</span><span class="sxs-lookup"><span data-stu-id="2fc72-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <ServerFarmWithRichSku>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fc72-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2fc72-107">DESCRIPTION</span></span>
<span data-ttu-id="2fc72-108">Das Cmdlet **Remove-AzureRmAppServicePlan** entfernt einen Azure App-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="2fc72-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="2fc72-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2fc72-109">EXAMPLES</span></span>

### <span data-ttu-id="2fc72-110">Beispiel 1: Entfernen eines App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="2fc72-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="2fc72-111">Mit diesem Befehl wird der Azure App-Service Plan mit dem Namen ContosoASP entfernt, der zur Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="2fc72-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="2fc72-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fc72-112">PARAMETERS</span></span>

### <span data-ttu-id="2fc72-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2fc72-113">-AppServicePlan</span></span>
<span data-ttu-id="2fc72-114">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="2fc72-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="2fc72-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2fc72-115">-Force</span></span>
<span data-ttu-id="2fc72-116">Option "gewaltsam entfernen"</span><span class="sxs-lookup"><span data-stu-id="2fc72-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="2fc72-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2fc72-117">-Name</span></span>
<span data-ttu-id="2fc72-118">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="2fc72-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="2fc72-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fc72-119">-ResourceGroupName</span></span>
<span data-ttu-id="2fc72-120">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="2fc72-120">Resource Group Name</span></span>

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

### <span data-ttu-id="2fc72-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2fc72-121">-Confirm</span></span>
<span data-ttu-id="2fc72-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fc72-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc72-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fc72-123">-WhatIf</span></span>
<span data-ttu-id="2fc72-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fc72-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fc72-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fc72-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc72-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc72-126">-DefaultProfile</span></span>
<span data-ttu-id="2fc72-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2fc72-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fc72-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc72-128">CommonParameters</span></span>
<span data-ttu-id="2fc72-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fc72-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc72-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fc72-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc72-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2fc72-131">INPUTS</span></span>

### <span data-ttu-id="2fc72-132">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="2fc72-132">ServerFarmWithRichSku</span></span>
<span data-ttu-id="2fc72-133">Der Parameter "AppServicePlan" akzeptiert den Wert vom Typ "ServerFarmWithRichSku" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2fc72-133">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="2fc72-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2fc72-134">OUTPUTS</span></span>

### <span data-ttu-id="2fc72-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2fc72-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="2fc72-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="2fc72-136">NOTES</span></span>

## <span data-ttu-id="2fc72-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2fc72-137">RELATED LINKS</span></span>

[<span data-ttu-id="2fc72-138">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2fc72-138">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="2fc72-139">Neu – AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2fc72-139">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="2fc72-140">Satz-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2fc72-140">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


