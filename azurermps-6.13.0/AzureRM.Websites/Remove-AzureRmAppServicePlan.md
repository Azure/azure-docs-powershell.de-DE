---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: b97506b8f104859c54c55ee1a937916623f4201d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477537"
---
# <span data-ttu-id="0b230-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0b230-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="0b230-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b230-102">SYNOPSIS</span></span>
<span data-ttu-id="0b230-103">Entfernt einen Azure App-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="0b230-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b230-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b230-104">SYNTAX</span></span>

### <span data-ttu-id="0b230-105">S1</span><span class="sxs-lookup"><span data-stu-id="0b230-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b230-106">S2</span><span class="sxs-lookup"><span data-stu-id="0b230-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b230-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b230-107">DESCRIPTION</span></span>
<span data-ttu-id="0b230-108">Das Cmdlet **Remove-AzureRmAppServicePlan** entfernt einen Azure App-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="0b230-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="0b230-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b230-109">EXAMPLES</span></span>

### <span data-ttu-id="0b230-110">Beispiel 1: Entfernen eines App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="0b230-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="0b230-111">Mit diesem Befehl wird der Azure App-Service Plan mit dem Namen ContosoASP entfernt, der zur Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="0b230-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="0b230-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b230-112">PARAMETERS</span></span>

### <span data-ttu-id="0b230-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0b230-113">-AppServicePlan</span></span>
<span data-ttu-id="0b230-114">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="0b230-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="0b230-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b230-115">-AsJob</span></span>
<span data-ttu-id="0b230-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0b230-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b230-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b230-117">-DefaultProfile</span></span>
<span data-ttu-id="0b230-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b230-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b230-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0b230-119">-Force</span></span>
<span data-ttu-id="0b230-120">Option "gewaltsam entfernen"</span><span class="sxs-lookup"><span data-stu-id="0b230-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="0b230-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0b230-121">-Name</span></span>
<span data-ttu-id="0b230-122">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="0b230-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="0b230-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b230-123">-ResourceGroupName</span></span>
<span data-ttu-id="0b230-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="0b230-124">Resource Group Name</span></span>

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

### <span data-ttu-id="0b230-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b230-125">-Confirm</span></span>
<span data-ttu-id="0b230-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b230-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b230-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b230-127">-WhatIf</span></span>
<span data-ttu-id="0b230-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b230-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b230-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b230-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b230-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b230-130">CommonParameters</span></span>
<span data-ttu-id="0b230-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b230-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b230-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b230-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b230-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b230-133">INPUTS</span></span>

### <span data-ttu-id="0b230-134">Microsoft. Azure. Management. Websites. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0b230-134">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="0b230-135">Parameter: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0b230-135">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="0b230-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b230-136">OUTPUTS</span></span>

### <span data-ttu-id="0b230-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0b230-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="0b230-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b230-138">NOTES</span></span>

## <span data-ttu-id="0b230-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b230-139">RELATED LINKS</span></span>

[<span data-ttu-id="0b230-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0b230-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="0b230-141">Neu – AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0b230-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="0b230-142">Satz-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0b230-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


