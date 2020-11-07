---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 971e96b61b22bd5efbd22b82468d864a63392a16
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819399"
---
# <span data-ttu-id="8b4c7-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="8b4c7-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="8b4c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b4c7-102">SYNOPSIS</span></span>
<span data-ttu-id="8b4c7-103">Mit diesem Cmdlet wird der aktuelle Wert der generierten Interchange Control Number pro Vereinbarung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="8b4c7-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="8b4c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b4c7-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b4c7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b4c7-105">DESCRIPTION</span></span>
<span data-ttu-id="8b4c7-106">Dieses Cmdlet soll in Disaster Recovery-Szenarien verwendet werden, um den aktuellen Wert der generierten Interchange-Steuerelementnummer abzurufen, damit ein höherer Wert mit "AzIntegrationAccountGeneratedIcn" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8b4c7-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="8b4c7-107">Die Austauschkontrollnummer sollte erhöht werden, um doppelte Austauschkontrollnummern für die Nummern zu vermeiden, die noch nicht in den passiven Bereich repliziert werden konnten, als das Desaster im aktiven Bereich stattfand.</span><span class="sxs-lookup"><span data-stu-id="8b4c7-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="8b4c7-108">Geben Sie den Parameter "-agreementtype" an, um anzugeben, ob X12-oder EDIFACT-Steuernummern zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8b4c7-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="8b4c7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b4c7-109">EXAMPLES</span></span>

### <span data-ttu-id="8b4c7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8b4c7-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="8b4c7-111">Mit diesem Befehl wird das für das Integration-Konto generierte X12 Interchange Control Number nach Vertragsname abgerufen.</span><span class="sxs-lookup"><span data-stu-id="8b4c7-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="8b4c7-112">Bitte stellen Sie sicher, dass die angegebene Vereinbarung den Typ "X12" hat.</span><span class="sxs-lookup"><span data-stu-id="8b4c7-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="8b4c7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8b4c7-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="8b4c7-114">Dieser Befehl ruft die vom Integration Account generierte EDIFACT Interchange Control Number nach Vertragsname ab.</span><span class="sxs-lookup"><span data-stu-id="8b4c7-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="8b4c7-115">Bitte stellen Sie sicher, dass die angegebene Vereinbarung den Typ "EDIFACT" hat.</span><span class="sxs-lookup"><span data-stu-id="8b4c7-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="8b4c7-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="8b4c7-116">Example 3</span></span>
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

<span data-ttu-id="8b4c7-117">Dieser Befehl ruft alle generierten X12 Interchange-Steuerelement Nummern nach dem Namen des Integrations Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="8b4c7-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="8b4c7-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b4c7-118">PARAMETERS</span></span>

### <span data-ttu-id="8b4c7-119">-Vertragsname</span><span class="sxs-lookup"><span data-stu-id="8b4c7-119">-AgreementName</span></span>
<span data-ttu-id="8b4c7-120">Der Name des Integrations kontovertrags.</span><span class="sxs-lookup"><span data-stu-id="8b4c7-120">The integration account agreement name.</span></span>

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

### <span data-ttu-id="8b4c7-121">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="8b4c7-121">-AgreementType</span></span>
<span data-ttu-id="8b4c7-122">Der Typ des Integrations kontovertrags.</span><span class="sxs-lookup"><span data-stu-id="8b4c7-122">The integration account agreement type.</span></span>

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

### <span data-ttu-id="8b4c7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b4c7-123">-DefaultProfile</span></span>
<span data-ttu-id="8b4c7-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8b4c7-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b4c7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8b4c7-125">-Name</span></span>
<span data-ttu-id="8b4c7-126">Der Name des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="8b4c7-126">The integration account name.</span></span>

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

### <span data-ttu-id="8b4c7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b4c7-127">-ResourceGroupName</span></span>
<span data-ttu-id="8b4c7-128">Der Name der Ressourcengruppe der Integrations Konten.</span><span class="sxs-lookup"><span data-stu-id="8b4c7-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="8b4c7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b4c7-129">CommonParameters</span></span>
<span data-ttu-id="8b4c7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b4c7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b4c7-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b4c7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b4c7-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b4c7-132">INPUTS</span></span>

### <span data-ttu-id="8b4c7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8b4c7-133">System.String</span></span>

## <span data-ttu-id="8b4c7-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b4c7-134">OUTPUTS</span></span>

### <span data-ttu-id="8b4c7-135">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="8b4c7-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="8b4c7-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b4c7-136">NOTES</span></span>

## <span data-ttu-id="8b4c7-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b4c7-137">RELATED LINKS</span></span>

[<span data-ttu-id="8b4c7-138">Satz-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="8b4c7-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

