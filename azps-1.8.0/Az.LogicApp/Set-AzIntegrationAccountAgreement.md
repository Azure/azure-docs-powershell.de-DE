---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
ms.openlocfilehash: fa03a9a14c8024298656de1ed8bcf97bbf65378c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819271"
---
# <span data-ttu-id="e16c6-101">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="e16c6-101">Set-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="e16c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e16c6-102">SYNOPSIS</span></span>
<span data-ttu-id="e16c6-103">Ändert eine Integration-Kontovereinbarung.</span><span class="sxs-lookup"><span data-stu-id="e16c6-103">Modifies an integration account agreement.</span></span>

## <span data-ttu-id="e16c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e16c6-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e16c6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e16c6-105">DESCRIPTION</span></span>
<span data-ttu-id="e16c6-106">Das Cmdlet " **Satz-AzIntegrationAccountAgreement** " ändert eine Integration-Kontovereinbarung.</span><span class="sxs-lookup"><span data-stu-id="e16c6-106">The **Set-AzIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="e16c6-107">Dieses Cmdlet gibt ein Objekt zurück, das die Integrations Kontovereinbarung darstellt.</span><span class="sxs-lookup"><span data-stu-id="e16c6-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="e16c6-108">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Vertragsnamen an.</span><span class="sxs-lookup"><span data-stu-id="e16c6-108">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="e16c6-109">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="e16c6-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="e16c6-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="e16c6-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e16c6-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="e16c6-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e16c6-112">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="e16c6-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e16c6-113">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="e16c6-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e16c6-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e16c6-114">EXAMPLES</span></span>

### <span data-ttu-id="e16c6-115">Beispiel 1: Aktualisieren einer Integration-Kontovereinbarung</span><span class="sxs-lookup"><span data-stu-id="e16c6-115">Example 1: Update an integration account agreement</span></span>
```
PS C:\>Set-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/agreements/IntegrationAccountAgreement06
Name                   : IntegrationAccountAgreement06
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/26/2016 6:43:52 PM
ChangedTime            : 3/26/2016 6:43:52 PM
AgreementType          : X12
HostPartner            : HostPartner
GuestPartner           : GuestPartner
HostIdentityQualifier  : AA
HostIdentityValue      : AA
GuestIdentityQualifier : BB
GuestIdentityValue     : BB
Content                : {"AS2":null,"X12":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ","Valu
                         e":"ZZ"},"ProtocolSettings":{"ValidationSettings":{"ValidateCharacterSet":true,"CheckDuplicateInterchangeControlNumber":false,"InterchangeControlN
                         . . .
```

<span data-ttu-id="e16c6-116">Dieser Befehl aktualisiert eine Integration-Kontovereinbarung in der angegebenen Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e16c6-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="e16c6-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="e16c6-117">PARAMETERS</span></span>

### <span data-ttu-id="e16c6-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="e16c6-118">-AgreementContent</span></span>
<span data-ttu-id="e16c6-119">Gibt den Vertragsinhalt im JSON-Format (JavaScript Object Notation) für die Vereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="e16c6-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="e16c6-120">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="e16c6-120">-AgreementContentFilePath</span></span>
<span data-ttu-id="e16c6-121">Gibt den Dateipfad der Vereinbarungs Inhalte an.</span><span class="sxs-lookup"><span data-stu-id="e16c6-121">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="e16c6-122">-Vertragsname</span><span class="sxs-lookup"><span data-stu-id="e16c6-122">-AgreementName</span></span>
<span data-ttu-id="e16c6-123">Gibt den Namen der Integrations Kontovereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="e16c6-123">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="e16c6-124">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="e16c6-124">-AgreementType</span></span>
<span data-ttu-id="e16c6-125">Gibt den Typ der Integrations Kontovereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="e16c6-125">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="e16c6-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e16c6-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e16c6-127">X12</span><span class="sxs-lookup"><span data-stu-id="e16c6-127">X12</span></span> 
- <span data-ttu-id="e16c6-128">AS2</span><span class="sxs-lookup"><span data-stu-id="e16c6-128">AS2</span></span>
- <span data-ttu-id="e16c6-129">EDIFACT</span><span class="sxs-lookup"><span data-stu-id="e16c6-129">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16c6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e16c6-130">-DefaultProfile</span></span>
<span data-ttu-id="e16c6-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e16c6-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e16c6-132">-Force</span><span class="sxs-lookup"><span data-stu-id="e16c6-132">-Force</span></span>
<span data-ttu-id="e16c6-133">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="e16c6-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16c6-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="e16c6-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="e16c6-135">Gibt einen Namen Business Identity Qualifier für den Gast Partner an.</span><span class="sxs-lookup"><span data-stu-id="e16c6-135">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="e16c6-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="e16c6-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="e16c6-137">Der Integrations Konto-Vereinbarungs Wert des Gast Identitäts Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="e16c6-137">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="e16c6-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="e16c6-138">-GuestPartner</span></span>
<span data-ttu-id="e16c6-139">Gibt den Namen des Gast Partners an.</span><span class="sxs-lookup"><span data-stu-id="e16c6-139">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="e16c6-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="e16c6-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="e16c6-141">Gibt einen Namen Business Identity Qualifier für den Host Partner an.</span><span class="sxs-lookup"><span data-stu-id="e16c6-141">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="e16c6-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="e16c6-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="e16c6-143">Der Integrations Kontovereinbarung-Wert des Host Identitäts Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="e16c6-143">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="e16c6-144">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="e16c6-144">-HostPartner</span></span>
<span data-ttu-id="e16c6-145">Gibt den Namen des Host Partners an.</span><span class="sxs-lookup"><span data-stu-id="e16c6-145">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="e16c6-146">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="e16c6-146">-Metadata</span></span>
<span data-ttu-id="e16c6-147">Gibt ein Metadaten-Objekt für die Vereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="e16c6-147">Specifies a metadata object for the agreement.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16c6-148">-Name</span><span class="sxs-lookup"><span data-stu-id="e16c6-148">-Name</span></span>
<span data-ttu-id="e16c6-149">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="e16c6-149">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e16c6-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e16c6-150">-ResourceGroupName</span></span>
<span data-ttu-id="e16c6-151">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e16c6-151">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e16c6-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e16c6-152">-Confirm</span></span>
<span data-ttu-id="e16c6-153">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e16c6-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e16c6-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e16c6-154">-WhatIf</span></span>
<span data-ttu-id="e16c6-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e16c6-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e16c6-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e16c6-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e16c6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e16c6-157">CommonParameters</span></span>
<span data-ttu-id="e16c6-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e16c6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e16c6-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e16c6-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e16c6-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e16c6-160">INPUTS</span></span>

### <span data-ttu-id="e16c6-161">System. String</span><span class="sxs-lookup"><span data-stu-id="e16c6-161">System.String</span></span>

## <span data-ttu-id="e16c6-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e16c6-162">OUTPUTS</span></span>

### <span data-ttu-id="e16c6-163">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="e16c6-163">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="e16c6-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="e16c6-164">NOTES</span></span>

## <span data-ttu-id="e16c6-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e16c6-165">RELATED LINKS</span></span>

[<span data-ttu-id="e16c6-166">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="e16c6-166">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="e16c6-167">Neu – AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="e16c6-167">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="e16c6-168">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="e16c6-168">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)


