---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 43806326f572030997299353cfc7e79e5587a4ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157729"
---
# <span data-ttu-id="93371-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="93371-101">Get-AzDefault</span></span>

## <span data-ttu-id="93371-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93371-102">SYNOPSIS</span></span>
<span data-ttu-id="93371-103">Holen Sie sich die vom Benutzer im aktuellen Kontext festgelegten Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="93371-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="93371-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93371-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93371-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93371-105">DESCRIPTION</span></span>
<span data-ttu-id="93371-106">Das Get-AzDefault ruft die Ressourcengruppe ab, die der Benutzer im aktuellen Kontext als Standard festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="93371-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="93371-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="93371-107">EXAMPLES</span></span>

### <span data-ttu-id="93371-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="93371-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="93371-109">Dieser Befehl gibt die aktuellen Standardwerte zurück, wenn Standardwerte festgelegt sind, oder nichts, wenn kein Standardwert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="93371-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="93371-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="93371-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="93371-111">Dieser Befehl gibt die aktuelle Standardressourcengruppe zurück, wenn ein Standardsatz festgelegt ist, oder nichts, wenn kein Standardwert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="93371-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="93371-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93371-112">PARAMETERS</span></span>

### <span data-ttu-id="93371-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93371-113">-DefaultProfile</span></span>
<span data-ttu-id="93371-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93371-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93371-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="93371-115">-ResourceGroup</span></span>
<span data-ttu-id="93371-116">Standardressourcengruppe anzeigen</span><span class="sxs-lookup"><span data-stu-id="93371-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="93371-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93371-117">CommonParameters</span></span>
<span data-ttu-id="93371-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93371-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93371-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93371-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93371-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="93371-120">INPUTS</span></span>

### <span data-ttu-id="93371-121">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="93371-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="93371-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="93371-122">OUTPUTS</span></span>

### <span data-ttu-id="93371-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="93371-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="93371-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="93371-124">NOTES</span></span>

## <span data-ttu-id="93371-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="93371-125">RELATED LINKS</span></span>
