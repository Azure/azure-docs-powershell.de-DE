---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 86eb9f1389f0474fcc109b219e9eae1bd385b7b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938859"
---
# <span data-ttu-id="23ad0-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="23ad0-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="23ad0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23ad0-102">SYNOPSIS</span></span>
<span data-ttu-id="23ad0-103">Entfernt eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="23ad0-103">Removes a snapshot.</span></span>

## <span data-ttu-id="23ad0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23ad0-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23ad0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23ad0-105">DESCRIPTION</span></span>
<span data-ttu-id="23ad0-106">Das **Cmdlet Remove-AzSnapshot** entfernt eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="23ad0-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="23ad0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="23ad0-107">EXAMPLES</span></span>

### <span data-ttu-id="23ad0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="23ad0-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="23ad0-109">Mit diesem Befehl wird die Momentaufnahme mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="23ad0-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="23ad0-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="23ad0-110">PARAMETERS</span></span>

### <span data-ttu-id="23ad0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23ad0-111">-AsJob</span></span>
<span data-ttu-id="23ad0-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="23ad0-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="23ad0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ad0-113">-DefaultProfile</span></span>
<span data-ttu-id="23ad0-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23ad0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23ad0-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="23ad0-115">-Force</span></span>
<span data-ttu-id="23ad0-116">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="23ad0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="23ad0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23ad0-117">-ResourceGroupName</span></span>
<span data-ttu-id="23ad0-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="23ad0-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="23ad0-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="23ad0-119">-SnapshotName</span></span>
<span data-ttu-id="23ad0-120">Gibt den Namen einer Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="23ad0-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23ad0-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="23ad0-121">-Confirm</span></span>
<span data-ttu-id="23ad0-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23ad0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23ad0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23ad0-123">-WhatIf</span></span>
<span data-ttu-id="23ad0-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23ad0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23ad0-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23ad0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23ad0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ad0-126">CommonParameters</span></span>
<span data-ttu-id="23ad0-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23ad0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ad0-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23ad0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ad0-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="23ad0-129">INPUTS</span></span>

### <span data-ttu-id="23ad0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="23ad0-130">System.String</span></span>

## <span data-ttu-id="23ad0-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="23ad0-131">OUTPUTS</span></span>

### <span data-ttu-id="23ad0-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="23ad0-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="23ad0-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="23ad0-133">NOTES</span></span>

## <span data-ttu-id="23ad0-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="23ad0-134">RELATED LINKS</span></span>
