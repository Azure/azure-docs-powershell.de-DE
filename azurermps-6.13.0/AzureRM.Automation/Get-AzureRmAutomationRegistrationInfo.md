---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
ms.openlocfilehash: 84332967eadfdb2accd12cc2f6f840ee337f92ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477998"
---
# <span data-ttu-id="9a616-101">Get-AzureRmAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="9a616-101">Get-AzureRmAutomationRegistrationInfo</span></span>

## <span data-ttu-id="9a616-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a616-102">SYNOPSIS</span></span>
<span data-ttu-id="9a616-103">Ruft Registrierungsinformationen für Onboarding eines DSC-Knotens oder einer hybriden Arbeitskraft zu Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="9a616-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a616-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a616-104">SYNTAX</span></span>

```
Get-AzureRmAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a616-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a616-105">DESCRIPTION</span></span>
<span data-ttu-id="9a616-106">Das Cmdlet " **Get-AzureRmAutomationRegistrationInfo** " Ruft den Endpunkt und die Schlüssel ab, die für die Onboard-Anforderung eines Status Konfigurations Knotens oder einer hybriden Arbeitskraft in ein Azure-Automatisierungs Konto erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9a616-106">The **Get-AzureRmAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="9a616-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a616-107">EXAMPLES</span></span>

### <span data-ttu-id="9a616-108">Beispiel 1: Abrufen von Registrierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="9a616-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzureRmAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="9a616-109">Dieser Befehl ruft die Registrierungsinformationen für das Automatisierungs Konto mit dem Namen AutomationAccount01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab.</span><span class="sxs-lookup"><span data-stu-id="9a616-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="9a616-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a616-110">PARAMETERS</span></span>

### <span data-ttu-id="9a616-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9a616-111">-AutomationAccountName</span></span>
<span data-ttu-id="9a616-112">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet Registrierungsinformationen erhält.</span><span class="sxs-lookup"><span data-stu-id="9a616-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="9a616-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a616-113">-DefaultProfile</span></span>
<span data-ttu-id="9a616-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9a616-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a616-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a616-115">-ResourceGroupName</span></span>
<span data-ttu-id="9a616-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9a616-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9a616-117">Dieses Cmdlet ruft Registrierungsinformationen für die Ressourcengruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9a616-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9a616-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a616-118">CommonParameters</span></span>
<span data-ttu-id="9a616-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a616-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a616-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a616-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a616-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a616-121">INPUTS</span></span>

### <span data-ttu-id="9a616-122">System. String</span><span class="sxs-lookup"><span data-stu-id="9a616-122">System.String</span></span>

## <span data-ttu-id="9a616-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a616-123">OUTPUTS</span></span>

### <span data-ttu-id="9a616-124">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="9a616-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="9a616-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a616-125">NOTES</span></span>

## <span data-ttu-id="9a616-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a616-126">RELATED LINKS</span></span>

[<span data-ttu-id="9a616-127">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9a616-127">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="9a616-128">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9a616-128">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="9a616-129">Neu – AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="9a616-129">New-AzureRmAutomationKey</span></span>](./New-AzureRmAutomationKey.md)


