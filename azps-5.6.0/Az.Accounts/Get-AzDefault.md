---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: aa1bfb0760480d5c2e24e113653037ecb83a9f6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949824"
---
# <span data-ttu-id="92bc6-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="92bc6-101">Get-AzDefault</span></span>

## <span data-ttu-id="92bc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92bc6-102">SYNOPSIS</span></span>
<span data-ttu-id="92bc6-103">Holen Sie sich die vom Benutzer im aktuellen Kontext festgelegten Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="92bc6-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="92bc6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92bc6-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92bc6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92bc6-105">DESCRIPTION</span></span>
<span data-ttu-id="92bc6-106">Das Get-AzDefault-Cmdlet ruft die Ressourcengruppe ab, die der Benutzer im aktuellen Kontext als Standard festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="92bc6-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="92bc6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="92bc6-107">EXAMPLES</span></span>

### <span data-ttu-id="92bc6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="92bc6-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="92bc6-109">Dieser Befehl gibt die aktuellen Standardwerte zurück, wenn Standardwerte festgelegt sind, oder gibt nichts zurück, wenn keine Standardeinstellung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="92bc6-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="92bc6-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="92bc6-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="92bc6-111">Dieser Befehl gibt die aktuelle Standardressourcengruppe zurück, wenn ein Standardsatz festgelegt ist, oder gibt nichts zurück, wenn kein Standardwert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="92bc6-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="92bc6-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="92bc6-112">PARAMETERS</span></span>

### <span data-ttu-id="92bc6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92bc6-113">-DefaultProfile</span></span>
<span data-ttu-id="92bc6-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92bc6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92bc6-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="92bc6-115">-ResourceGroup</span></span>
<span data-ttu-id="92bc6-116">Standardressourcengruppe anzeigen</span><span class="sxs-lookup"><span data-stu-id="92bc6-116">Display Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92bc6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92bc6-117">CommonParameters</span></span>
<span data-ttu-id="92bc6-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92bc6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92bc6-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92bc6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92bc6-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="92bc6-120">INPUTS</span></span>

### <span data-ttu-id="92bc6-121">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="92bc6-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="92bc6-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="92bc6-122">OUTPUTS</span></span>

### <span data-ttu-id="92bc6-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="92bc6-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="92bc6-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="92bc6-124">NOTES</span></span>

## <span data-ttu-id="92bc6-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="92bc6-125">RELATED LINKS</span></span>
