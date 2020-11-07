---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 374a43b6b094622808f4704daf7063a4c4c0c153
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658461"
---
# <span data-ttu-id="a9607-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="a9607-101">Get-AzDefault</span></span>

## <span data-ttu-id="a9607-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9607-102">SYNOPSIS</span></span>
<span data-ttu-id="a9607-103">Rufen Sie die vom Benutzer im aktuellen Kontext gesetzten Standardwerte ab.</span><span class="sxs-lookup"><span data-stu-id="a9607-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="a9607-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9607-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9607-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9607-105">DESCRIPTION</span></span>
<span data-ttu-id="a9607-106">Das Get-AzDefault-Cmdlet ruft die Ressourcengruppe ab, die der Benutzer im aktuellen Kontext als Standard festgesetzt hat.</span><span class="sxs-lookup"><span data-stu-id="a9607-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="a9607-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9607-107">EXAMPLES</span></span>

### <span data-ttu-id="a9607-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9607-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="a9607-109">Dieser Befehl gibt die aktuellen Standardwerte zurück, wenn Standardwerte gesetzt sind, oder gibt Nothing zurück, wenn kein Standardwert gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="a9607-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="a9607-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a9607-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="a9607-111">Dieser Befehl gibt die aktuelle Standardressourcen Gruppe zurück, wenn ein Standardsatz vorhanden ist, oder gibt Nothing zurück, wenn kein Standardwert gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="a9607-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="a9607-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9607-112">PARAMETERS</span></span>

### <span data-ttu-id="a9607-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9607-113">-DefaultProfile</span></span>
<span data-ttu-id="a9607-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9607-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9607-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a9607-115">-ResourceGroup</span></span>
<span data-ttu-id="a9607-116">Standardressourcen Gruppe anzeigen</span><span class="sxs-lookup"><span data-stu-id="a9607-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="a9607-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9607-117">CommonParameters</span></span>
<span data-ttu-id="a9607-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9607-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9607-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9607-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9607-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9607-120">INPUTS</span></span>

### <span data-ttu-id="a9607-121">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="a9607-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a9607-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9607-122">OUTPUTS</span></span>

### <span data-ttu-id="a9607-123">Microsoft. Azure. Commands. profile. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a9607-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="a9607-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9607-124">NOTES</span></span>

## <span data-ttu-id="a9607-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9607-125">RELATED LINKS</span></span>
