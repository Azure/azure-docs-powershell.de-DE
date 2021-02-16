---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: 35e767c340d5418ae500c4cc87a4b40741d8ba6a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171162"
---
# <span data-ttu-id="2c513-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="2c513-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="2c513-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c513-102">SYNOPSIS</span></span>
<span data-ttu-id="2c513-103">Widerruft den Zugriff auf eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="2c513-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="2c513-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c513-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c513-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c513-105">DESCRIPTION</span></span>
<span data-ttu-id="2c513-106">Das **Cmdlet Revoke-AzSnapshotAccess** widerruft den Zugriff auf eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="2c513-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="2c513-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2c513-107">EXAMPLES</span></span>

### <span data-ttu-id="2c513-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2c513-108">Example 1</span></span>
```
PS C:\> Revoke-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="2c513-109">Widerrufen des Zugriffs auf die Momentaufnahme mit dem Namen 'Snapshot01' in der Ressourcengruppe namens 'ResourceGroup01'</span><span class="sxs-lookup"><span data-stu-id="2c513-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="2c513-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c513-110">PARAMETERS</span></span>

### <span data-ttu-id="2c513-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c513-111">-AsJob</span></span>
<span data-ttu-id="2c513-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2c513-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c513-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c513-113">-DefaultProfile</span></span>
<span data-ttu-id="2c513-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c513-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c513-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c513-115">-ResourceGroupName</span></span>
<span data-ttu-id="2c513-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2c513-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2c513-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="2c513-117">-SnapshotName</span></span>
<span data-ttu-id="2c513-118">Gibt den Namen einer Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="2c513-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="2c513-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c513-119">-Confirm</span></span>
<span data-ttu-id="2c513-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2c513-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c513-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2c513-121">-WhatIf</span></span>
<span data-ttu-id="2c513-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2c513-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c513-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c513-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c513-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c513-124">CommonParameters</span></span>
<span data-ttu-id="2c513-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c513-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c513-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c513-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c513-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2c513-127">INPUTS</span></span>

### <span data-ttu-id="2c513-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2c513-128">System.String</span></span>

## <span data-ttu-id="2c513-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2c513-129">OUTPUTS</span></span>

### <span data-ttu-id="2c513-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="2c513-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2c513-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2c513-131">NOTES</span></span>

## <span data-ttu-id="2c513-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2c513-132">RELATED LINKS</span></span>
