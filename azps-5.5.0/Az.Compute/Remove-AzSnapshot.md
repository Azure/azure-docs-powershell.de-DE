---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 686f7dbe4bba17017e1920dd2c67a05c2ccd5eae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171198"
---
# <span data-ttu-id="4fbed-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="4fbed-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="4fbed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fbed-102">SYNOPSIS</span></span>
<span data-ttu-id="4fbed-103">Entfernt eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="4fbed-103">Removes a snapshot.</span></span>

## <span data-ttu-id="4fbed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4fbed-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fbed-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4fbed-105">DESCRIPTION</span></span>
<span data-ttu-id="4fbed-106">Das **Cmdlet "Remove-AzSnapshot"** entfernt eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="4fbed-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="4fbed-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4fbed-107">EXAMPLES</span></span>

### <span data-ttu-id="4fbed-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4fbed-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="4fbed-109">Mit diesem Befehl wird die Momentaufnahme mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="4fbed-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4fbed-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fbed-110">PARAMETERS</span></span>

### <span data-ttu-id="4fbed-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fbed-111">-AsJob</span></span>
<span data-ttu-id="4fbed-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="4fbed-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4fbed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fbed-113">-DefaultProfile</span></span>
<span data-ttu-id="4fbed-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4fbed-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fbed-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4fbed-115">-Force</span></span>
<span data-ttu-id="4fbed-116">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="4fbed-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4fbed-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fbed-117">-ResourceGroupName</span></span>
<span data-ttu-id="4fbed-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4fbed-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4fbed-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="4fbed-119">-SnapshotName</span></span>
<span data-ttu-id="4fbed-120">Gibt den Namen einer Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="4fbed-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="4fbed-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fbed-121">-Confirm</span></span>
<span data-ttu-id="4fbed-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4fbed-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fbed-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4fbed-123">-WhatIf</span></span>
<span data-ttu-id="4fbed-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4fbed-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fbed-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4fbed-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fbed-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fbed-126">CommonParameters</span></span>
<span data-ttu-id="4fbed-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fbed-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fbed-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fbed-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fbed-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4fbed-129">INPUTS</span></span>

### <span data-ttu-id="4fbed-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4fbed-130">System.String</span></span>

## <span data-ttu-id="4fbed-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4fbed-131">OUTPUTS</span></span>

### <span data-ttu-id="4fbed-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="4fbed-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4fbed-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4fbed-133">NOTES</span></span>

## <span data-ttu-id="4fbed-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4fbed-134">RELATED LINKS</span></span>
