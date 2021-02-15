---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: 226791db9057fe0f8aa246fab546dd4af7303529
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166892"
---
# <span data-ttu-id="ddf4f-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="ddf4f-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="ddf4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddf4f-102">SYNOPSIS</span></span>
<span data-ttu-id="ddf4f-103">Ruft Registrierungsinformationen für das Onboarding eines DSC-Knotens oder hybriden Workers in die Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="ddf4f-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="ddf4f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ddf4f-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddf4f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddf4f-105">DESCRIPTION</span></span>
<span data-ttu-id="ddf4f-106">Das **Cmdlet "Get-AzAutomationRegistrationInfo"** ruft den Endpunkt und die Schlüssel ab, die zum Integrieren eines Knotens (Desired State Configuration, DSC) oder eines Hybrid-Workers in ein Azure-Automatisierungskonto erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ddf4f-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="ddf4f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ddf4f-107">EXAMPLES</span></span>

### <span data-ttu-id="ddf4f-108">Beispiel 1: Informationen zur Registrierung</span><span class="sxs-lookup"><span data-stu-id="ddf4f-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="ddf4f-109">Dieser Befehl ruft die Registrierungsinformationen für das Automatisierungskonto namens AutomationAccount01 in der Ressourcengruppe mit dem Namen "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="ddf4f-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="ddf4f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddf4f-110">PARAMETERS</span></span>

### <span data-ttu-id="ddf4f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ddf4f-111">-AutomationAccountName</span></span>
<span data-ttu-id="ddf4f-112">Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet Registrierungsinformationen erhält.</span><span class="sxs-lookup"><span data-stu-id="ddf4f-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="ddf4f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddf4f-113">-DefaultProfile</span></span>
<span data-ttu-id="ddf4f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ddf4f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddf4f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddf4f-115">-ResourceGroupName</span></span>
<span data-ttu-id="ddf4f-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ddf4f-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ddf4f-117">Dieses Cmdlet ruft Registrierungsinformationen für die Ressourcengruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ddf4f-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ddf4f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddf4f-118">CommonParameters</span></span>
<span data-ttu-id="ddf4f-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddf4f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddf4f-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddf4f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddf4f-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ddf4f-121">INPUTS</span></span>

### <span data-ttu-id="ddf4f-122">System.String</span><span class="sxs-lookup"><span data-stu-id="ddf4f-122">System.String</span></span>

## <span data-ttu-id="ddf4f-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ddf4f-123">OUTPUTS</span></span>

### <span data-ttu-id="ddf4f-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="ddf4f-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="ddf4f-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ddf4f-125">NOTES</span></span>

## <span data-ttu-id="ddf4f-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ddf4f-126">RELATED LINKS</span></span>

[<span data-ttu-id="ddf4f-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ddf4f-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="ddf4f-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ddf4f-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="ddf4f-129">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="ddf4f-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)


