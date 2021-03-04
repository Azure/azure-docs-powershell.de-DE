---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: a4b4e5048e4d11a5b376650b94520232f10b29bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937096"
---
# <span data-ttu-id="4a2fb-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4a2fb-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="4a2fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a2fb-102">SYNOPSIS</span></span>
<span data-ttu-id="4a2fb-103">Entfernt einen Verfügbarkeitssatz aus Azure.</span><span class="sxs-lookup"><span data-stu-id="4a2fb-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="4a2fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a2fb-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a2fb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a2fb-105">DESCRIPTION</span></span>
<span data-ttu-id="4a2fb-106">Das **Cmdlet Remove-AzAvailabilitySet** entfernt einen Verfügbarkeitssatz aus Azure.</span><span class="sxs-lookup"><span data-stu-id="4a2fb-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="4a2fb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a2fb-107">EXAMPLES</span></span>

### <span data-ttu-id="4a2fb-108">Beispiel 1: Entfernen eines Verfügbarkeitssets</span><span class="sxs-lookup"><span data-stu-id="4a2fb-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="4a2fb-109">Mit diesem Befehl wird ein Verfügbarkeitssatz mit dem Namen AvailabilitySet03 in der Ressourcengruppe "ResourceGroup11" entfernt.</span><span class="sxs-lookup"><span data-stu-id="4a2fb-109">This command removes an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="4a2fb-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4a2fb-110">PARAMETERS</span></span>

### <span data-ttu-id="4a2fb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a2fb-111">-AsJob</span></span>
<span data-ttu-id="4a2fb-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="4a2fb-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4a2fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a2fb-113">-DefaultProfile</span></span>
<span data-ttu-id="4a2fb-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a2fb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a2fb-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="4a2fb-115">-Force</span></span>
<span data-ttu-id="4a2fb-116">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="4a2fb-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a2fb-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4a2fb-117">-Name</span></span>
<span data-ttu-id="4a2fb-118">Der Name des Verfügbarkeitssatzs.</span><span class="sxs-lookup"><span data-stu-id="4a2fb-118">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a2fb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a2fb-119">-ResourceGroupName</span></span>
<span data-ttu-id="4a2fb-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4a2fb-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a2fb-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4a2fb-121">-Confirm</span></span>
<span data-ttu-id="4a2fb-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4a2fb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a2fb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a2fb-123">-WhatIf</span></span>
<span data-ttu-id="4a2fb-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a2fb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a2fb-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a2fb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a2fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a2fb-126">CommonParameters</span></span>
<span data-ttu-id="4a2fb-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a2fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a2fb-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a2fb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a2fb-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a2fb-129">INPUTS</span></span>

### <span data-ttu-id="4a2fb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4a2fb-130">System.String</span></span>

## <span data-ttu-id="4a2fb-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a2fb-131">OUTPUTS</span></span>

### <span data-ttu-id="4a2fb-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4a2fb-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="4a2fb-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4a2fb-133">NOTES</span></span>

## <span data-ttu-id="4a2fb-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4a2fb-134">RELATED LINKS</span></span>

[<span data-ttu-id="4a2fb-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4a2fb-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="4a2fb-136">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4a2fb-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


