---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 95c2b33b52ed9660c57aad35128af4eba277c0a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501790"
---
# <span data-ttu-id="b627e-101">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="b627e-101">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="b627e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b627e-102">SYNOPSIS</span></span>
<span data-ttu-id="b627e-103">Dieses Cmdlet entfernt eine bestimmte empfangene Austauschkontrollnummer pro Vereinbarung und Steuernummern Wert.</span><span class="sxs-lookup"><span data-stu-id="b627e-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b627e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b627e-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b627e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b627e-105">DESCRIPTION</span></span>
<span data-ttu-id="b627e-106">Dieses Cmdlet ist für die Verwendung in Disaster Recovery-Szenarien vorgesehen, um eine empfangene Interchange-Kontrollnummer aus dem Integration-Konto zu entfernen, damit der B2B-Connector die Nachricht erneut verarbeiten kann, wenn die Erkennung doppelter Nummern aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b627e-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="b627e-107">In seltenen Fällen kann die empfangene Interchange-Kontrollnummer kurz vor einem Notfall reserviert werden, bevor der B2B-Connector den Austausch als fehlerhaft ablehnt.</span><span class="sxs-lookup"><span data-stu-id="b627e-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="b627e-108">In solchen Fällen kann es sein, dass der Vorgang die Wiederherstellungs Website aktivieren soll, um denselben Austausch erneut zu verarbeiten, nachdem die Nutzlast korrigiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b627e-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="b627e-109">Geben Sie den Parameter "-agreementtype" an, um anzugeben, ob X12-oder EDIFACT-Steuernummern zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b627e-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="b627e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b627e-110">EXAMPLES</span></span>

### <span data-ttu-id="b627e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b627e-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The existing recevied control number '000000641' for agreement 'X12AgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The session 'X12-ICN-X12AgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="b627e-112">Versucht, eine empfangene X12 Interchange-Steuerelementnummer abzurufen, deren Inhalt kein gültiges Format aufweist.</span><span class="sxs-lookup"><span data-stu-id="b627e-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="b627e-113">Entfernt die empfangene X12 Interchange-Kontrollnummer.</span><span class="sxs-lookup"><span data-stu-id="b627e-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="b627e-114">Bestätigt, dass die empfangene X12 Interchange-Kontrollnummer entfernt wurde, indem Sie versuchen, Sie erneut zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b627e-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="b627e-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b627e-115">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The existing recevied control number '000000641' for agreement 'EdifactAgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The session 'Edifact-ICN-EdifactAgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="b627e-116">Versucht, eine empfangene EDIFACT-Austauschkontrollnummer abzurufen, deren Inhalt kein gültiges Format aufweist.</span><span class="sxs-lookup"><span data-stu-id="b627e-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="b627e-117">Entfernt die empfangene EDIFACT-Interchange-Kontrollnummer.</span><span class="sxs-lookup"><span data-stu-id="b627e-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="b627e-118">Bestätigt, dass die empfangene EDIFACT-Austauschkontrollnummer entfernt wurde, indem Sie versuchen, Sie erneut zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b627e-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="b627e-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="b627e-119">PARAMETERS</span></span>

### <span data-ttu-id="b627e-120">-Vertragsname</span><span class="sxs-lookup"><span data-stu-id="b627e-120">-AgreementName</span></span>
<span data-ttu-id="b627e-121">Der Name des Integrations kontovertrags.</span><span class="sxs-lookup"><span data-stu-id="b627e-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="b627e-122">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="b627e-122">-ControlNumberValue</span></span>
<span data-ttu-id="b627e-123">Der Wert des Integrations Konto-Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="b627e-123">The integration account control number value.</span></span>

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

### <span data-ttu-id="b627e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b627e-124">-Name</span></span>
<span data-ttu-id="b627e-125">Der Name des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="b627e-125">The integration account name.</span></span>

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

### <span data-ttu-id="b627e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b627e-126">-ResourceGroupName</span></span>
<span data-ttu-id="b627e-127">Der Name der Ressourcengruppe der Integrations Konten.</span><span class="sxs-lookup"><span data-stu-id="b627e-127">The integration account resource group name.</span></span>

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

### <span data-ttu-id="b627e-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b627e-128">-Confirm</span></span>
<span data-ttu-id="b627e-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b627e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b627e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b627e-130">-WhatIf</span></span>
<span data-ttu-id="b627e-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b627e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b627e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b627e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b627e-133">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="b627e-133">-AgreementType</span></span>
<span data-ttu-id="b627e-134">Der Typ des Integrations kontovertrags.</span><span class="sxs-lookup"><span data-stu-id="b627e-134">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b627e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b627e-135">-DefaultProfile</span></span>
<span data-ttu-id="b627e-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b627e-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b627e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b627e-137">CommonParameters</span></span>
<span data-ttu-id="b627e-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b627e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b627e-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b627e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b627e-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b627e-140">INPUTS</span></span>

### <span data-ttu-id="b627e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b627e-141">System.String</span></span>

## <span data-ttu-id="b627e-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b627e-142">OUTPUTS</span></span>

### <span data-ttu-id="b627e-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="b627e-143">System.Object</span></span>

## <span data-ttu-id="b627e-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="b627e-144">NOTES</span></span>

## <span data-ttu-id="b627e-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b627e-145">RELATED LINKS</span></span>

<span data-ttu-id="b627e-146">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md) 
 [Satz-AzureRmIntegrationAccountReceivedIcn](./Set-AzureRmIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="b627e-146">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md)
[Set-AzureRmIntegrationAccountReceivedIcn](./Set-AzureRmIntegrationAccountReceivedIcn.md)</span></span>

