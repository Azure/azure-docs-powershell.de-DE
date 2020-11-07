---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 15ecd8c0e22438016ea0f589cf798ecbcb65188f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847676"
---
# <span data-ttu-id="f42e7-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f42e7-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="f42e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f42e7-102">SYNOPSIS</span></span>
<span data-ttu-id="f42e7-103">Entfernt einen Verfügbarkeits Satz aus Azure.</span><span class="sxs-lookup"><span data-stu-id="f42e7-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="f42e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f42e7-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f42e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f42e7-105">DESCRIPTION</span></span>
<span data-ttu-id="f42e7-106">Das Cmdlet **Remove-AzAvailabilitySet** entfernt einen Verfügbarkeits Satz aus Azure.</span><span class="sxs-lookup"><span data-stu-id="f42e7-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="f42e7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f42e7-107">EXAMPLES</span></span>

### <span data-ttu-id="f42e7-108">Beispiel 1: Entfernen eines Verfügbarkeits Satzes</span><span class="sxs-lookup"><span data-stu-id="f42e7-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f42e7-109">Dieser Befehl entfernt einen Verfügbarkeits Satz mit dem Namen AvailabilitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f42e7-109">This command removes an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="f42e7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f42e7-110">PARAMETERS</span></span>

### <span data-ttu-id="f42e7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f42e7-111">-AsJob</span></span>
<span data-ttu-id="f42e7-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="f42e7-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f42e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f42e7-113">-DefaultProfile</span></span>
<span data-ttu-id="f42e7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f42e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f42e7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f42e7-115">-Force</span></span>
<span data-ttu-id="f42e7-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f42e7-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f42e7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f42e7-117">-Name</span></span>
<span data-ttu-id="f42e7-118">Der Name der verfügbarkeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f42e7-118">The availability set name.</span></span>

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

### <span data-ttu-id="f42e7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f42e7-119">-ResourceGroupName</span></span>
<span data-ttu-id="f42e7-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f42e7-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f42e7-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f42e7-121">-Confirm</span></span>
<span data-ttu-id="f42e7-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f42e7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f42e7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f42e7-123">-WhatIf</span></span>
<span data-ttu-id="f42e7-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f42e7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f42e7-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f42e7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f42e7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f42e7-126">CommonParameters</span></span>
<span data-ttu-id="f42e7-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f42e7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f42e7-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f42e7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f42e7-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f42e7-129">INPUTS</span></span>

### <span data-ttu-id="f42e7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f42e7-130">System.String</span></span>

## <span data-ttu-id="f42e7-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f42e7-131">OUTPUTS</span></span>

### <span data-ttu-id="f42e7-132">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f42e7-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f42e7-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="f42e7-133">NOTES</span></span>

## <span data-ttu-id="f42e7-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f42e7-134">RELATED LINKS</span></span>

[<span data-ttu-id="f42e7-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f42e7-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="f42e7-136">Neu – AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f42e7-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


