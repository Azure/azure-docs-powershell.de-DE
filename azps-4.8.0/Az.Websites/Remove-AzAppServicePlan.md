---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: dfd2cfd20ab11e2e70e03dc3e166c83729ef344a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166709"
---
# <span data-ttu-id="0d942-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0d942-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="0d942-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d942-102">SYNOPSIS</span></span>
<span data-ttu-id="0d942-103">Entfernt einen Azure App-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="0d942-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="0d942-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d942-104">SYNTAX</span></span>

### <span data-ttu-id="0d942-105">S1</span><span class="sxs-lookup"><span data-stu-id="0d942-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d942-106">S2</span><span class="sxs-lookup"><span data-stu-id="0d942-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d942-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d942-107">DESCRIPTION</span></span>
<span data-ttu-id="0d942-108">Das Cmdlet **Remove-AzAppServicePlan** entfernt einen Azure App-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="0d942-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="0d942-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d942-109">EXAMPLES</span></span>

### <span data-ttu-id="0d942-110">Beispiel 1: Entfernen eines App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="0d942-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="0d942-111">Mit diesem Befehl wird der Azure App-Service Plan mit dem Namen ContosoASP entfernt, der zur Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="0d942-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="0d942-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d942-112">PARAMETERS</span></span>

### <span data-ttu-id="0d942-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0d942-113">-AppServicePlan</span></span>
<span data-ttu-id="0d942-114">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="0d942-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="0d942-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d942-115">-AsJob</span></span>
<span data-ttu-id="0d942-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0d942-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d942-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d942-117">-DefaultProfile</span></span>
<span data-ttu-id="0d942-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d942-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d942-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0d942-119">-Force</span></span>
<span data-ttu-id="0d942-120">Option "gewaltsam entfernen"</span><span class="sxs-lookup"><span data-stu-id="0d942-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="0d942-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0d942-121">-Name</span></span>
<span data-ttu-id="0d942-122">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="0d942-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="0d942-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d942-123">-ResourceGroupName</span></span>
<span data-ttu-id="0d942-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="0d942-124">Resource Group Name</span></span>

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

### <span data-ttu-id="0d942-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0d942-125">-Confirm</span></span>
<span data-ttu-id="0d942-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d942-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d942-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d942-127">-WhatIf</span></span>
<span data-ttu-id="0d942-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d942-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d942-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d942-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d942-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d942-130">CommonParameters</span></span>
<span data-ttu-id="0d942-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d942-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d942-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d942-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d942-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d942-133">INPUTS</span></span>

### <span data-ttu-id="0d942-134">Microsoft. Azure. Commands. webapps. Models. PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="0d942-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="0d942-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d942-135">OUTPUTS</span></span>

### <span data-ttu-id="0d942-136">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0d942-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="0d942-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d942-137">NOTES</span></span>

## <span data-ttu-id="0d942-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d942-138">RELATED LINKS</span></span>

[<span data-ttu-id="0d942-139">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0d942-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="0d942-140">Neu – AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0d942-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="0d942-141">Satz-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0d942-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


