---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: 226791db9057fe0f8aa246fab546dd4af7303529
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008161"
---
# <span data-ttu-id="e1173-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="e1173-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="e1173-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1173-102">SYNOPSIS</span></span>
<span data-ttu-id="e1173-103">Ruft Registrierungsinformationen für Onboarding eines DSC-Knotens oder einer hybriden Arbeitskraft zu Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="e1173-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="e1173-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1173-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1173-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1173-105">DESCRIPTION</span></span>
<span data-ttu-id="e1173-106">Das Cmdlet " **Get-AzAutomationRegistrationInfo** " Ruft den Endpunkt und die Schlüssel ab, die für die Onboard-Anforderung eines Status Konfigurations Knotens oder einer hybriden Arbeitskraft in ein Azure-Automatisierungs Konto erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e1173-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="e1173-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1173-107">EXAMPLES</span></span>

### <span data-ttu-id="e1173-108">Beispiel 1: Abrufen von Registrierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="e1173-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="e1173-109">Dieser Befehl ruft die Registrierungsinformationen für das Automatisierungs Konto mit dem Namen AutomationAccount01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab.</span><span class="sxs-lookup"><span data-stu-id="e1173-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="e1173-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1173-110">PARAMETERS</span></span>

### <span data-ttu-id="e1173-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e1173-111">-AutomationAccountName</span></span>
<span data-ttu-id="e1173-112">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet Registrierungsinformationen erhält.</span><span class="sxs-lookup"><span data-stu-id="e1173-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="e1173-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1173-113">-DefaultProfile</span></span>
<span data-ttu-id="e1173-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e1173-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1173-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1173-115">-ResourceGroupName</span></span>
<span data-ttu-id="e1173-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e1173-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e1173-117">Dieses Cmdlet ruft Registrierungsinformationen für die Ressourcengruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e1173-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e1173-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1173-118">CommonParameters</span></span>
<span data-ttu-id="e1173-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1173-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1173-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1173-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1173-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1173-121">INPUTS</span></span>

### <span data-ttu-id="e1173-122">System. String</span><span class="sxs-lookup"><span data-stu-id="e1173-122">System.String</span></span>

## <span data-ttu-id="e1173-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1173-123">OUTPUTS</span></span>

### <span data-ttu-id="e1173-124">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="e1173-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="e1173-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1173-125">NOTES</span></span>

## <span data-ttu-id="e1173-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1173-126">RELATED LINKS</span></span>

[<span data-ttu-id="e1173-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e1173-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="e1173-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="e1173-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="e1173-129">Neu – AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="e1173-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)


