---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: ee581528810663d09fe724f370b681ff9e20072f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469159"
---
# <span data-ttu-id="f3ae4-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="f3ae4-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="f3ae4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ae4-103">Entfernt alle AzureRm-Module von einem Computer.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="f3ae4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3ae4-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3ae4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3ae4-105">DESCRIPTION</span></span>
<span data-ttu-id="f3ae4-106">Entfernt alle AzureRm-Module von einem Computer.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="f3ae4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f3ae4-107">EXAMPLES</span></span>

### <span data-ttu-id="f3ae4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f3ae4-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="f3ae4-109">Durch Ausführen dieses Befehls werden alle AzureRm-Module vom Computer für die Version von PowerShell entfernt, in der das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="f3ae4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3ae4-110">PARAMETERS</span></span>

### <span data-ttu-id="f3ae4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ae4-111">-DefaultProfile</span></span>
<span data-ttu-id="f3ae4-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3ae4-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3ae4-113">-PassThru</span></span>
<span data-ttu-id="f3ae4-114">Rückgabeliste von Modulen, die bei Angabe entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="f3ae4-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3ae4-115">-Confirm</span></span>
<span data-ttu-id="f3ae4-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3ae4-117">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f3ae4-117">-WhatIf</span></span>
<span data-ttu-id="f3ae4-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3ae4-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3ae4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ae4-120">CommonParameters</span></span>
<span data-ttu-id="f3ae4-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ae4-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3ae4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ae4-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f3ae4-123">INPUTS</span></span>

### <span data-ttu-id="f3ae4-124">Keine</span><span class="sxs-lookup"><span data-stu-id="f3ae4-124">None</span></span>

## <span data-ttu-id="f3ae4-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f3ae4-125">OUTPUTS</span></span>

### <span data-ttu-id="f3ae4-126">System.String</span><span class="sxs-lookup"><span data-stu-id="f3ae4-126">System.String</span></span>

## <span data-ttu-id="f3ae4-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f3ae4-127">NOTES</span></span>

## <span data-ttu-id="f3ae4-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f3ae4-128">RELATED LINKS</span></span>
