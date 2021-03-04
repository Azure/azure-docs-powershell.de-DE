---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServiceEnvironment.md
ms.openlocfilehash: 9641c55dd25d8f09d1898bdda37fafa840db0a19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934563"
---
# <span data-ttu-id="b09e9-101">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="b09e9-101">Get-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="b09e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b09e9-102">SYNOPSIS</span></span>
<span data-ttu-id="b09e9-103">Ruft die App-Dienstumgebung ab.</span><span class="sxs-lookup"><span data-stu-id="b09e9-103">Gets App Service Environment.</span></span> <span data-ttu-id="b09e9-104">Wenn nur Ressourcengruppe angegeben ist, gibt sie eine Liste von ASE in der Ressourcengruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="b09e9-104">If only Resource Group is specified, it will return a list of ASE in the Resource Group.</span></span>

## <span data-ttu-id="b09e9-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b09e9-105">SYNTAX</span></span>

```
Get-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b09e9-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b09e9-106">DESCRIPTION</span></span>
<span data-ttu-id="b09e9-107">Das **Get-AzAppServiceEnvironment-Cmdlet** gibt ASE(n) zurück, die der Abfrage entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b09e9-107">The **Get-AzAppServiceEnvironment** cmdlet return ASE(s) matching the query.</span></span>

## <span data-ttu-id="b09e9-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b09e9-108">EXAMPLES</span></span>

### <span data-ttu-id="b09e9-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b09e9-109">Example 1</span></span>
```powershell
PS C:\> Get-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseName
```

<span data-ttu-id="b09e9-110">Gibt eine bestimmte App-Dienstumgebung mit dem <MyAseName> Namen in zurück. <MyResourceGroup></span><span class="sxs-lookup"><span data-stu-id="b09e9-110">Returns a specific App Service Environment named <MyAseName> in <MyResourceGroup></span></span>

## <span data-ttu-id="b09e9-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b09e9-111">PARAMETERS</span></span>

### <span data-ttu-id="b09e9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b09e9-112">-DefaultProfile</span></span>
<span data-ttu-id="b09e9-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b09e9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b09e9-114">-Name</span><span class="sxs-lookup"><span data-stu-id="b09e9-114">-Name</span></span>
<span data-ttu-id="b09e9-115">Der Name der App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="b09e9-115">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b09e9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b09e9-116">-ResourceGroupName</span></span>
<span data-ttu-id="b09e9-117">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b09e9-117">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b09e9-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b09e9-118">-Confirm</span></span>
<span data-ttu-id="b09e9-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b09e9-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b09e9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b09e9-120">-WhatIf</span></span>
<span data-ttu-id="b09e9-121">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b09e9-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b09e9-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b09e9-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b09e9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b09e9-123">CommonParameters</span></span>
<span data-ttu-id="b09e9-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b09e9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b09e9-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b09e9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b09e9-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b09e9-126">INPUTS</span></span>

### <span data-ttu-id="b09e9-127">Keine</span><span class="sxs-lookup"><span data-stu-id="b09e9-127">None</span></span>

## <span data-ttu-id="b09e9-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b09e9-128">OUTPUTS</span></span>

### <span data-ttu-id="b09e9-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="b09e9-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment</span></span>

## <span data-ttu-id="b09e9-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b09e9-130">NOTES</span></span>

## <span data-ttu-id="b09e9-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b09e9-131">RELATED LINKS</span></span>

[<span data-ttu-id="b09e9-132">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="b09e9-132">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="b09e9-133">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="b09e9-133">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)

[<span data-ttu-id="b09e9-134">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="b09e9-134">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)