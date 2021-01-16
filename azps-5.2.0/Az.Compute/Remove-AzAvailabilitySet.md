---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 15ecd8c0e22438016ea0f589cf798ecbcb65188f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292810"
---
# <span data-ttu-id="5844f-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5844f-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="5844f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5844f-102">SYNOPSIS</span></span>
<span data-ttu-id="5844f-103">Entfernt einen Verfügbarkeitssatz aus Azure.</span><span class="sxs-lookup"><span data-stu-id="5844f-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="5844f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5844f-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5844f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5844f-105">DESCRIPTION</span></span>
<span data-ttu-id="5844f-106">Das **Cmdlet "Remove-AzAvailabilitySet"** entfernt einen Verfügbarkeitssatz aus Azure.</span><span class="sxs-lookup"><span data-stu-id="5844f-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="5844f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5844f-107">EXAMPLES</span></span>

### <span data-ttu-id="5844f-108">Beispiel 1: Entfernen eines Verfügbarkeitssets</span><span class="sxs-lookup"><span data-stu-id="5844f-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="5844f-109">Mit diesem Befehl wird ein Verfügbarkeitssatz namens "AvailabilitySet03" in der Ressourcengruppe "ResourceGroup11" entfernt.</span><span class="sxs-lookup"><span data-stu-id="5844f-109">This command removes an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="5844f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5844f-110">PARAMETERS</span></span>

### <span data-ttu-id="5844f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5844f-111">-AsJob</span></span>
<span data-ttu-id="5844f-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="5844f-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5844f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5844f-113">-DefaultProfile</span></span>
<span data-ttu-id="5844f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5844f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5844f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5844f-115">-Force</span></span>
<span data-ttu-id="5844f-116">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="5844f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5844f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5844f-117">-Name</span></span>
<span data-ttu-id="5844f-118">Der Name des Verfügbarkeitssatzs.</span><span class="sxs-lookup"><span data-stu-id="5844f-118">The availability set name.</span></span>

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

### <span data-ttu-id="5844f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5844f-119">-ResourceGroupName</span></span>
<span data-ttu-id="5844f-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5844f-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5844f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5844f-121">-Confirm</span></span>
<span data-ttu-id="5844f-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5844f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5844f-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5844f-123">-WhatIf</span></span>
<span data-ttu-id="5844f-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5844f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5844f-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5844f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5844f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5844f-126">CommonParameters</span></span>
<span data-ttu-id="5844f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5844f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5844f-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5844f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5844f-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5844f-129">INPUTS</span></span>

### <span data-ttu-id="5844f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5844f-130">System.String</span></span>

## <span data-ttu-id="5844f-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5844f-131">OUTPUTS</span></span>

### <span data-ttu-id="5844f-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5844f-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5844f-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5844f-133">NOTES</span></span>

## <span data-ttu-id="5844f-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5844f-134">RELATED LINKS</span></span>

[<span data-ttu-id="5844f-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5844f-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="5844f-136">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5844f-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


