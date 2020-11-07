---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 3e929d2df0b2132b89f6ccff6b83020453b61ad2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841060"
---
# <span data-ttu-id="79c5e-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="79c5e-101">Get-AzDefault</span></span>

## <span data-ttu-id="79c5e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="79c5e-103">Rufen Sie die vom Benutzer im aktuellen Kontext gesetzten Standardwerte ab.</span><span class="sxs-lookup"><span data-stu-id="79c5e-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="79c5e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79c5e-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79c5e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79c5e-105">DESCRIPTION</span></span>
<span data-ttu-id="79c5e-106">Das Get-AzDefault-Cmdlet ruft die Ressourcengruppe ab, die der Benutzer im aktuellen Kontext als Standard festgesetzt hat.</span><span class="sxs-lookup"><span data-stu-id="79c5e-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="79c5e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79c5e-107">EXAMPLES</span></span>

### <span data-ttu-id="79c5e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="79c5e-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="79c5e-109">Dieser Befehl gibt die aktuellen Standardwerte zurück, wenn Standardwerte gesetzt sind, oder gibt Nothing zurück, wenn kein Standardwert gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="79c5e-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="79c5e-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="79c5e-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="79c5e-111">Dieser Befehl gibt die aktuelle Standardressourcen Gruppe zurück, wenn ein Standardsatz vorhanden ist, oder gibt Nothing zurück, wenn kein Standardwert gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="79c5e-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="79c5e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="79c5e-112">PARAMETERS</span></span>

### <span data-ttu-id="79c5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c5e-113">-DefaultProfile</span></span>
<span data-ttu-id="79c5e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="79c5e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79c5e-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="79c5e-115">-ResourceGroup</span></span>
<span data-ttu-id="79c5e-116">Standardressourcen Gruppe anzeigen</span><span class="sxs-lookup"><span data-stu-id="79c5e-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="79c5e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c5e-117">CommonParameters</span></span>
<span data-ttu-id="79c5e-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c5e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c5e-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79c5e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c5e-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79c5e-120">INPUTS</span></span>

### <span data-ttu-id="79c5e-121">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="79c5e-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="79c5e-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79c5e-122">OUTPUTS</span></span>

### <span data-ttu-id="79c5e-123">Microsoft. Azure. Commands. profile. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="79c5e-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="79c5e-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="79c5e-124">NOTES</span></span>

## <span data-ttu-id="79c5e-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79c5e-125">RELATED LINKS</span></span>
