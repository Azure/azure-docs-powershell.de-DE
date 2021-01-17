---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: ed10bd42fb52515cb05adadfc69ee4f1620150e3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471314"
---
# <span data-ttu-id="455f7-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="455f7-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="455f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="455f7-102">SYNOPSIS</span></span>
<span data-ttu-id="455f7-103">Generiert die Registrierungsschlüssel für ein Automatisierungskonto erneut.</span><span class="sxs-lookup"><span data-stu-id="455f7-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="455f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="455f7-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="455f7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="455f7-105">DESCRIPTION</span></span>
<span data-ttu-id="455f7-106">Das **Cmdlet "New-AzAutomationKey"** generiert registrierungsschlüssel für ein Azure-Automatisierungskonto erneut.</span><span class="sxs-lookup"><span data-stu-id="455f7-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="455f7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="455f7-107">EXAMPLES</span></span>

### <span data-ttu-id="455f7-108">Beispiel 1: Neuer erstellen eines Schlüssels für ein Automatisierungskonto</span><span class="sxs-lookup"><span data-stu-id="455f7-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="455f7-109">Mit diesem Befehl wird der Primärschlüssel für das Azure-Automatisierungskonto mit dem Namen "AutomationAccount01" in der Ressourcengruppe "ResourceGroup01" erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="455f7-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="455f7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="455f7-110">PARAMETERS</span></span>

### <span data-ttu-id="455f7-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="455f7-111">-AutomationAccountName</span></span>
<span data-ttu-id="455f7-112">Gibt den Namen eines Automatisierungskontos an, für das dieses Cmdlet Schlüssel erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="455f7-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="455f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="455f7-113">-DefaultProfile</span></span>
<span data-ttu-id="455f7-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="455f7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="455f7-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="455f7-115">-KeyType</span></span>
<span data-ttu-id="455f7-116">Gibt den Typ des Agentregistrierungsschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="455f7-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="455f7-117">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="455f7-117">Valid values are:</span></span> 
- <span data-ttu-id="455f7-118">Primär</span><span class="sxs-lookup"><span data-stu-id="455f7-118">Primary</span></span> 
- <span data-ttu-id="455f7-119">Sekundär</span><span class="sxs-lookup"><span data-stu-id="455f7-119">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="455f7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="455f7-120">-ResourceGroupName</span></span>
<span data-ttu-id="455f7-121">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="455f7-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="455f7-122">Dieses Cmdlet generiert erneut Schlüssel für ein Automatisierungskonto in der Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="455f7-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="455f7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="455f7-123">CommonParameters</span></span>
<span data-ttu-id="455f7-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="455f7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="455f7-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="455f7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="455f7-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="455f7-126">INPUTS</span></span>

### <span data-ttu-id="455f7-127">System.String</span><span class="sxs-lookup"><span data-stu-id="455f7-127">System.String</span></span>

## <span data-ttu-id="455f7-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="455f7-128">OUTPUTS</span></span>

### <span data-ttu-id="455f7-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="455f7-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="455f7-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="455f7-130">NOTES</span></span>

## <span data-ttu-id="455f7-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="455f7-131">RELATED LINKS</span></span>
