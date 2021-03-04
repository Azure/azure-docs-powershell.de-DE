---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 78478b28e42302ad3a672a0ee889f03807f3d1ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935752"
---
# <span data-ttu-id="e92a7-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="e92a7-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="e92a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e92a7-102">SYNOPSIS</span></span>
<span data-ttu-id="e92a7-103">Löscht einen IotHub.</span><span class="sxs-lookup"><span data-stu-id="e92a7-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="e92a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e92a7-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e92a7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e92a7-105">DESCRIPTION</span></span>
<span data-ttu-id="e92a7-106">Löscht einen IotHub.</span><span class="sxs-lookup"><span data-stu-id="e92a7-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="e92a7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e92a7-107">EXAMPLES</span></span>

### <span data-ttu-id="e92a7-108">Beispiel 1 Entfernen eines IotHub</span><span class="sxs-lookup"><span data-stu-id="e92a7-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e92a7-109">Entfernt einen IotHub mit dem Namen "myiothub"</span><span class="sxs-lookup"><span data-stu-id="e92a7-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="e92a7-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e92a7-110">PARAMETERS</span></span>

### <span data-ttu-id="e92a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e92a7-111">-DefaultProfile</span></span>
<span data-ttu-id="e92a7-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e92a7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e92a7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e92a7-113">-Name</span></span>
<span data-ttu-id="e92a7-114">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="e92a7-114">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e92a7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e92a7-115">-ResourceGroupName</span></span>
<span data-ttu-id="e92a7-116">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="e92a7-116">Resource Group Name</span></span>

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

### <span data-ttu-id="e92a7-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e92a7-117">-Confirm</span></span>
<span data-ttu-id="e92a7-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e92a7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e92a7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e92a7-119">-WhatIf</span></span>
<span data-ttu-id="e92a7-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e92a7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e92a7-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e92a7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e92a7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e92a7-122">CommonParameters</span></span>
<span data-ttu-id="e92a7-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e92a7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e92a7-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e92a7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e92a7-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e92a7-125">INPUTS</span></span>

### <span data-ttu-id="e92a7-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e92a7-126">System.String</span></span>

## <span data-ttu-id="e92a7-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e92a7-127">OUTPUTS</span></span>

### <span data-ttu-id="e92a7-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="e92a7-128">System.Void</span></span>

## <span data-ttu-id="e92a7-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e92a7-129">NOTES</span></span>

## <span data-ttu-id="e92a7-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e92a7-130">RELATED LINKS</span></span>
