---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: b6bf2c126a1009d824ab8bae1ea2e2031459d876
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922920"
---
# <span data-ttu-id="052b5-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="052b5-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="052b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="052b5-102">SYNOPSIS</span></span>
<span data-ttu-id="052b5-103">Dieses Cmdlet ruft den aktuellen Wert der generierten Austauschsteuerelementnummer pro Vereinbarung ab.</span><span class="sxs-lookup"><span data-stu-id="052b5-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="052b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="052b5-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="052b5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="052b5-105">DESCRIPTION</span></span>
<span data-ttu-id="052b5-106">Dieses Cmdlet soll in Notfallwiederherstellungsszenarien verwendet werden, um den aktuellen Wert der generierten Austauschsteuerelementnummer abzurufen, um mit Set-AzIntegrationAccountGeneratedIcn einen erhöhten Wert zurückschreiben zu können.</span><span class="sxs-lookup"><span data-stu-id="052b5-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="052b5-107">Die Nummer des Austauschsteuerelements sollte erhöht werden, um doppelte Austauschsteuerungsnummern für die Nummern zu vermeiden, die noch nicht in den passiven Bereich repliziert werden konnten, als das Unglück in der aktiven Region passierte.</span><span class="sxs-lookup"><span data-stu-id="052b5-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="052b5-108">Geben Sie den Parameter "-AgreementType" an, um anzugeben, ob X12- oder Edifact-Steuerelementnummern</span><span class="sxs-lookup"><span data-stu-id="052b5-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="052b5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="052b5-109">EXAMPLES</span></span>

### <span data-ttu-id="052b5-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="052b5-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="052b5-111">Dieser Befehl ruft das integration account generated X12 interchange control number by agreement name ab.</span><span class="sxs-lookup"><span data-stu-id="052b5-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="052b5-112">Stellen Sie sicher, dass der angegebene Vertrag vom Typ "X12" ist.</span><span class="sxs-lookup"><span data-stu-id="052b5-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="052b5-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="052b5-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="052b5-114">Dieser Befehl ruft die generierte Edifact-Austauschsteuerelementnummer nach Vertragsname ab.</span><span class="sxs-lookup"><span data-stu-id="052b5-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="052b5-115">Stellen Sie sicher, dass die angegebene Vereinbarung vom Typ "Edifact" ist.</span><span class="sxs-lookup"><span data-stu-id="052b5-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="052b5-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="052b5-116">Example 3</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1"
ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement1
IsMessageProcessingFailed:

ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement2
IsMessageProcessingFailed:

ControlNumber            : No generated control number was found for this agreement.
ControlNumberChangedTime : 1/1/0001 12:00:00 AM
AgreementName            : X12IntegrationAccountAgreement3
IsMessageProcessingFailed:
```

<span data-ttu-id="052b5-117">Dieser Befehl ruft alle generierten X12-Austauschsteuerelementnummern nach dem Namen des Integrationskontos ab.</span><span class="sxs-lookup"><span data-stu-id="052b5-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="052b5-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="052b5-118">PARAMETERS</span></span>

### <span data-ttu-id="052b5-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="052b5-119">-AgreementName</span></span>
<span data-ttu-id="052b5-120">Der Name des Integrationskontovertrags.</span><span class="sxs-lookup"><span data-stu-id="052b5-120">The integration account agreement name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="052b5-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="052b5-121">-AgreementType</span></span>
<span data-ttu-id="052b5-122">Der Typ des Integrationskontovertrags.</span><span class="sxs-lookup"><span data-stu-id="052b5-122">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="052b5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="052b5-123">-DefaultProfile</span></span>
<span data-ttu-id="052b5-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="052b5-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="052b5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="052b5-125">-Name</span></span>
<span data-ttu-id="052b5-126">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="052b5-126">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="052b5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="052b5-127">-ResourceGroupName</span></span>
<span data-ttu-id="052b5-128">Name der Ressourcengruppe des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="052b5-128">The integration account resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="052b5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="052b5-129">CommonParameters</span></span>
<span data-ttu-id="052b5-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="052b5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="052b5-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="052b5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="052b5-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="052b5-132">INPUTS</span></span>

### <span data-ttu-id="052b5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="052b5-133">System.String</span></span>

## <span data-ttu-id="052b5-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="052b5-134">OUTPUTS</span></span>

### <span data-ttu-id="052b5-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="052b5-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="052b5-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="052b5-136">NOTES</span></span>

## <span data-ttu-id="052b5-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="052b5-137">RELATED LINKS</span></span>

[<span data-ttu-id="052b5-138">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="052b5-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

