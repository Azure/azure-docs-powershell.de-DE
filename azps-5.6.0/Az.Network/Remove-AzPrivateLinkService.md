---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: e06a29422a7abed55dbf1e8508c8715a36cf7d76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941523"
---
# <span data-ttu-id="46bd9-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46bd9-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="46bd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46bd9-102">SYNOPSIS</span></span>
<span data-ttu-id="46bd9-103">Entfernt einen privaten Linkdienst</span><span class="sxs-lookup"><span data-stu-id="46bd9-103">Removes a private link service</span></span>

## <span data-ttu-id="46bd9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46bd9-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46bd9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46bd9-105">DESCRIPTION</span></span>
<span data-ttu-id="46bd9-106">Das **Cmdlet Remove-AzPrivateLinkService** entfernt einen privaten Linkdienst.</span><span class="sxs-lookup"><span data-stu-id="46bd9-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="46bd9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="46bd9-107">EXAMPLES</span></span>

### <span data-ttu-id="46bd9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="46bd9-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="46bd9-109">In diesem Beispiel wird ein privater Linkdienst mit dem Namen TestPrivateLinkService entfernt.</span><span class="sxs-lookup"><span data-stu-id="46bd9-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="46bd9-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="46bd9-110">PARAMETERS</span></span>

### <span data-ttu-id="46bd9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46bd9-111">-AsJob</span></span>
<span data-ttu-id="46bd9-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="46bd9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46bd9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46bd9-113">-DefaultProfile</span></span>
<span data-ttu-id="46bd9-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46bd9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46bd9-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="46bd9-115">-Force</span></span>
<span data-ttu-id="46bd9-116">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="46bd9-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="46bd9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="46bd9-117">-Name</span></span>
<span data-ttu-id="46bd9-118">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="46bd9-118">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46bd9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46bd9-119">-PassThru</span></span>
<span data-ttu-id="46bd9-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="46bd9-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="46bd9-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="46bd9-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="46bd9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46bd9-122">-ResourceGroupName</span></span>
<span data-ttu-id="46bd9-123">Der Ressourcengruppenname des privaten Linkdiensts.</span><span class="sxs-lookup"><span data-stu-id="46bd9-123">The resource group name of the private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46bd9-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46bd9-124">-Confirm</span></span>
<span data-ttu-id="46bd9-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46bd9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46bd9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46bd9-126">-WhatIf</span></span>
<span data-ttu-id="46bd9-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46bd9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46bd9-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46bd9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46bd9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46bd9-129">CommonParameters</span></span>
<span data-ttu-id="46bd9-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46bd9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46bd9-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46bd9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46bd9-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="46bd9-132">INPUTS</span></span>

### <span data-ttu-id="46bd9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="46bd9-133">System.String</span></span>

## <span data-ttu-id="46bd9-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="46bd9-134">OUTPUTS</span></span>

### <span data-ttu-id="46bd9-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="46bd9-135">System.Boolean</span></span>

## <span data-ttu-id="46bd9-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="46bd9-136">NOTES</span></span>

## <span data-ttu-id="46bd9-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="46bd9-137">RELATED LINKS</span></span>

[<span data-ttu-id="46bd9-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46bd9-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="46bd9-139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46bd9-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)