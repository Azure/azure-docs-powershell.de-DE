---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 94cb9c54752b29da68beefa713894fd77a385b45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650708"
---
# <span data-ttu-id="12224-101">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="12224-101">Set-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="12224-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12224-102">SYNOPSIS</span></span>
<span data-ttu-id="12224-103">Aktualisiert das Integrations Konto, das ICN (Interchange Control Number) in der Azure-Ressourcengruppe erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="12224-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="12224-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12224-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12224-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12224-105">DESCRIPTION</span></span>
<span data-ttu-id="12224-106">Das Set-AzIntegrationAccountGeneratedIcn-Cmdlet aktualisiert ein vorhandenes Integration-Konto, das die Interchange Control Number (ICN) erhalten hat, und gibt ein Objekt zurück, das die Nummer des Austausch kontrollkontos des Integrations Kontos empfängt.</span><span class="sxs-lookup"><span data-stu-id="12224-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="12224-107">Verwenden Sie dieses Cmdlet, um den Nachrichten Verarbeitungsstatus eines Integrations Kontos zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="12224-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="12224-108">Sie können die Nummer eines Integration-Kontos, das die Austausch Steuerung erhalten hat, aktualisieren, indem Sie den Namen des Integrations Kontos, den Namen der Ressourcengruppe, den Namen der Vereinbarung, den Nummernwert und den Nachrichten Verarbeitungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="12224-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="12224-109">Mit diesem Befehl können Sie keine neue Integrations Konto-Nummer für das Integration-Konto erstellen.</span><span class="sxs-lookup"><span data-stu-id="12224-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="12224-110">Wenn Sie die dynamischen Parameter verwenden möchten, geben Sie Sie einfach in den Befehl ein, oder geben Sie einen Bindestrich (-) ein, um einen Parameternamen anzugeben, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="12224-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="12224-111">Wenn Sie einen erforderlichen Vorlagenparameter verpassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="12224-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="12224-112">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="12224-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="12224-113">Geben Sie den Parameter "-agreementtype" an, um anzugeben, ob X12-oder EDIFACT-Steuernummern zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="12224-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="12224-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12224-114">EXAMPLES</span></span>

### <span data-ttu-id="12224-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="12224-115">Example 1</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="12224-116">Mit diesem Befehl wird das Integration-Konto, das die X12 Interchange-Kontrollnummer erhalten hat, für eine bestimmte Integrations Kontovereinbarung und einen Wert mit dem Status der Nachrichtenverarbeitung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="12224-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="12224-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="12224-117">Example 2</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="12224-118">Mit diesem Befehl wird das Integrations Konto, das die EDIFACT-Interchange-Kontrollnummer erhalten hat, für eine bestimmte Integrations Kontovereinbarung und einen Wert mit dem Status Fehler bei der Nachrichtenverarbeitung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="12224-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="12224-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="12224-119">PARAMETERS</span></span>

### <span data-ttu-id="12224-120">-Vertragsname</span><span class="sxs-lookup"><span data-stu-id="12224-120">-AgreementName</span></span>
<span data-ttu-id="12224-121">Der Name des Integrations kontovertrags.</span><span class="sxs-lookup"><span data-stu-id="12224-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="12224-122">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="12224-122">-AgreementType</span></span>
<span data-ttu-id="12224-123">Der Typ des Integrations kontovertrags (X12 oder EDIFACT).</span><span class="sxs-lookup"><span data-stu-id="12224-123">The integration account agreement type (X12 or Edifact).</span></span>

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

### <span data-ttu-id="12224-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="12224-124">-ControlNumberValue</span></span>
<span data-ttu-id="12224-125">Der Wert des Integrations Konto-Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="12224-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="12224-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12224-126">-DefaultProfile</span></span>
<span data-ttu-id="12224-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="12224-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12224-128">-IsMessageProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="12224-128">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="12224-129">Der Status der empfangenen Nachrichtenverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="12224-129">The received message processing status.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12224-130">-Name</span><span class="sxs-lookup"><span data-stu-id="12224-130">-Name</span></span>
<span data-ttu-id="12224-131">Der Name des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="12224-131">The integration account name.</span></span>

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

### <span data-ttu-id="12224-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12224-132">-ResourceGroupName</span></span>
<span data-ttu-id="12224-133">Der Name der Ressourcengruppe der Integrations Konten.</span><span class="sxs-lookup"><span data-stu-id="12224-133">The integration account resource group name.</span></span>

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

### <span data-ttu-id="12224-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12224-134">-Confirm</span></span>
<span data-ttu-id="12224-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12224-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12224-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12224-136">-WhatIf</span></span>
<span data-ttu-id="12224-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12224-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12224-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12224-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12224-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12224-139">CommonParameters</span></span>
<span data-ttu-id="12224-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12224-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12224-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12224-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12224-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12224-142">INPUTS</span></span>

### <span data-ttu-id="12224-143">System. String</span><span class="sxs-lookup"><span data-stu-id="12224-143">System.String</span></span>

## <span data-ttu-id="12224-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12224-144">OUTPUTS</span></span>

### <span data-ttu-id="12224-145">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="12224-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="12224-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="12224-146">NOTES</span></span>

## <span data-ttu-id="12224-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12224-147">RELATED LINKS</span></span>

<span data-ttu-id="12224-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="12224-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span></span>
