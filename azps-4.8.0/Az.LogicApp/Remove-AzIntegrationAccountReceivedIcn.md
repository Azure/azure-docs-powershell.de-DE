---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 2a80173900c0faf062c3d4ba0c0a3b2029737bcf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174677"
---
# <span data-ttu-id="edefd-101">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="edefd-101">Remove-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="edefd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="edefd-102">SYNOPSIS</span></span>
<span data-ttu-id="edefd-103">Dieses Cmdlet entfernt eine bestimmte empfangene Austauschkontrollnummer pro Vereinbarung und Steuernummern Wert.</span><span class="sxs-lookup"><span data-stu-id="edefd-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="edefd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="edefd-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edefd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edefd-105">DESCRIPTION</span></span>
<span data-ttu-id="edefd-106">Dieses Cmdlet ist für die Verwendung in Disaster Recovery-Szenarien vorgesehen, um eine empfangene Interchange-Kontrollnummer aus dem Integration-Konto zu entfernen, damit der B2B-Connector die Nachricht erneut verarbeiten kann, wenn die Erkennung doppelter Nummern aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="edefd-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="edefd-107">In seltenen Fällen kann die empfangene Interchange-Kontrollnummer kurz vor einem Notfall reserviert werden, bevor der B2B-Connector den Austausch als fehlerhaft ablehnt.</span><span class="sxs-lookup"><span data-stu-id="edefd-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="edefd-108">In solchen Fällen kann es sein, dass der Vorgang die Wiederherstellungs Website aktivieren soll, um denselben Austausch erneut zu verarbeiten, nachdem die Nutzlast korrigiert wurde.</span><span class="sxs-lookup"><span data-stu-id="edefd-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="edefd-109">Geben Sie den Parameter "-agreementtype" an, um anzugeben, ob X12-oder EDIFACT-Steuernummern zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="edefd-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="edefd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="edefd-110">EXAMPLES</span></span>

### <span data-ttu-id="edefd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="edefd-111">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'X12AgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'X12-ICN-X12AgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="edefd-112">Versucht, eine empfangene X12 Interchange-Steuerelementnummer abzurufen, deren Inhalt kein gültiges Format aufweist.</span><span class="sxs-lookup"><span data-stu-id="edefd-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="edefd-113">Entfernt die empfangene X12 Interchange-Kontrollnummer.</span><span class="sxs-lookup"><span data-stu-id="edefd-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="edefd-114">Bestätigt, dass die empfangene X12 Interchange-Kontrollnummer entfernt wurde, indem Sie versuchen, Sie erneut zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="edefd-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="edefd-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="edefd-115">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'EdifactAgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'Edifact-ICN-EdifactAgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="edefd-116">Versucht, eine empfangene EDIFACT-Austauschkontrollnummer abzurufen, deren Inhalt kein gültiges Format aufweist.</span><span class="sxs-lookup"><span data-stu-id="edefd-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="edefd-117">Entfernt die empfangene EDIFACT-Interchange-Kontrollnummer.</span><span class="sxs-lookup"><span data-stu-id="edefd-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="edefd-118">Bestätigt, dass die empfangene EDIFACT-Austauschkontrollnummer entfernt wurde, indem Sie versuchen, Sie erneut zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="edefd-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="edefd-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="edefd-119">PARAMETERS</span></span>

### <span data-ttu-id="edefd-120">-Vertragsname</span><span class="sxs-lookup"><span data-stu-id="edefd-120">-AgreementName</span></span>
<span data-ttu-id="edefd-121">Der Name des Integrations kontovertrags.</span><span class="sxs-lookup"><span data-stu-id="edefd-121">The integration account agreement name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edefd-122">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="edefd-122">-AgreementType</span></span>
<span data-ttu-id="edefd-123">Der Typ des Integrations kontovertrags.</span><span class="sxs-lookup"><span data-stu-id="edefd-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="edefd-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="edefd-124">-ControlNumberValue</span></span>
<span data-ttu-id="edefd-125">Der Wert des Integrations Konto-Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="edefd-125">The integration account control number value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edefd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edefd-126">-DefaultProfile</span></span>
<span data-ttu-id="edefd-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="edefd-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edefd-128">-Name</span><span class="sxs-lookup"><span data-stu-id="edefd-128">-Name</span></span>
<span data-ttu-id="edefd-129">Der Name des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="edefd-129">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edefd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edefd-130">-ResourceGroupName</span></span>
<span data-ttu-id="edefd-131">Der Name der Ressourcengruppe der Integrations Konten.</span><span class="sxs-lookup"><span data-stu-id="edefd-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="edefd-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="edefd-132">-Confirm</span></span>
<span data-ttu-id="edefd-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="edefd-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edefd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edefd-134">-WhatIf</span></span>
<span data-ttu-id="edefd-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="edefd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edefd-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="edefd-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edefd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edefd-137">CommonParameters</span></span>
<span data-ttu-id="edefd-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edefd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edefd-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edefd-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edefd-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="edefd-140">INPUTS</span></span>

### <span data-ttu-id="edefd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="edefd-141">System.String</span></span>

## <span data-ttu-id="edefd-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="edefd-142">OUTPUTS</span></span>

### <span data-ttu-id="edefd-143">System. void</span><span class="sxs-lookup"><span data-stu-id="edefd-143">System.Void</span></span>

## <span data-ttu-id="edefd-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="edefd-144">NOTES</span></span>

## <span data-ttu-id="edefd-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="edefd-145">RELATED LINKS</span></span>

<span data-ttu-id="edefd-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Satz-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="edefd-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span></span>

