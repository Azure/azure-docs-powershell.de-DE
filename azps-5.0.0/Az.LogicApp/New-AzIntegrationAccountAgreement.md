---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 190745ce8b09bf29b3cc3cbc07f35899732f97f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180355"
---
# <span data-ttu-id="398a6-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="398a6-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="398a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="398a6-102">SYNOPSIS</span></span>
<span data-ttu-id="398a6-103">Erstellt eine Integrations Kontovereinbarung.</span><span class="sxs-lookup"><span data-stu-id="398a6-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="398a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="398a6-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="398a6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="398a6-105">DESCRIPTION</span></span>
<span data-ttu-id="398a6-106">Das Cmdlet **New-AzIntegrationAccountAgreement** erstellt eine Integrations Kontovereinbarung.</span><span class="sxs-lookup"><span data-stu-id="398a6-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="398a6-107">Dieses Cmdlet gibt ein Objekt zurück, das die Integrations Kontovereinbarung darstellt.</span><span class="sxs-lookup"><span data-stu-id="398a6-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="398a6-108">Geben Sie den Namen des Integrations Kontos, den Namen der Ressourcengruppe, den Namen der Vereinbarung, den Typ, den Partnernamen, die Partner Qualifizierer und den Vertragsinhalt an.</span><span class="sxs-lookup"><span data-stu-id="398a6-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="398a6-109">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="398a6-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="398a6-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="398a6-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="398a6-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="398a6-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="398a6-112">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="398a6-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="398a6-113">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="398a6-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="398a6-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="398a6-114">EXAMPLES</span></span>

### <span data-ttu-id="398a6-115">Beispiel 1: Erstellen einer Integrations Kontovereinbarung</span><span class="sxs-lookup"><span data-stu-id="398a6-115">Example 1: Create a integration account agreement</span></span>
```powershell
PS C:\>New-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="398a6-116">Mit diesem Befehl wird eine Integration-Kontovereinbarung in der angegebenen Azure-Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="398a6-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="398a6-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="398a6-117">Example 2</span></span>

<span data-ttu-id="398a6-118">Erstellt eine Integrations Kontovereinbarung.</span><span class="sxs-lookup"><span data-stu-id="398a6-118">Creates an integration account agreement.</span></span> <span data-ttu-id="398a6-119">automatisch</span><span class="sxs-lookup"><span data-stu-id="398a6-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountAgreement -AgreementContent <String> -AgreementName 'IntegrationAccountAgreement06' -AgreementType X12 -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="398a6-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="398a6-120">PARAMETERS</span></span>

### <span data-ttu-id="398a6-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="398a6-121">-AgreementContent</span></span>
<span data-ttu-id="398a6-122">Gibt den Vertragsinhalt im JSON-Format (JavaScript Object Notation) für die Vereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="398a6-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="398a6-123">Geben Sie entweder diesen Parameter oder den *AgreementContentFilePath* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="398a6-123">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="398a6-124">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="398a6-124">-AgreementContentFilePath</span></span>
<span data-ttu-id="398a6-125">Gibt den Dateipfad der Vereinbarungs Inhalte an.</span><span class="sxs-lookup"><span data-stu-id="398a6-125">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="398a6-126">Geben Sie entweder diesen Parameter oder den *AgreementContent* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="398a6-126">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="398a6-127">-Vertragsname</span><span class="sxs-lookup"><span data-stu-id="398a6-127">-AgreementName</span></span>
<span data-ttu-id="398a6-128">Gibt einen Namen für die Integrations Kontovereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="398a6-128">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="398a6-129">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="398a6-129">-AgreementType</span></span>
<span data-ttu-id="398a6-130">Gibt den Typ der Integrations Kontovereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="398a6-130">Specifies the integration account agreement type.</span></span> <span data-ttu-id="398a6-131">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="398a6-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="398a6-132">X12</span><span class="sxs-lookup"><span data-stu-id="398a6-132">X12</span></span> 
- <span data-ttu-id="398a6-133">AS2</span><span class="sxs-lookup"><span data-stu-id="398a6-133">AS2</span></span>
- <span data-ttu-id="398a6-134">EDIFACT</span><span class="sxs-lookup"><span data-stu-id="398a6-134">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="398a6-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="398a6-135">-DefaultProfile</span></span>
<span data-ttu-id="398a6-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="398a6-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="398a6-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="398a6-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="398a6-138">Gibt einen Namen Business Identity Qualifier für den Gast Partner an.</span><span class="sxs-lookup"><span data-stu-id="398a6-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="398a6-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="398a6-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="398a6-140">Der Integrations Konto-Vereinbarungs Wert des Gast Identitäts Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="398a6-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="398a6-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="398a6-141">-GuestPartner</span></span>
<span data-ttu-id="398a6-142">Gibt den Namen des Gast Partners an.</span><span class="sxs-lookup"><span data-stu-id="398a6-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="398a6-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="398a6-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="398a6-144">Gibt einen Namen Business Identity Qualifier für den Host Partner an.</span><span class="sxs-lookup"><span data-stu-id="398a6-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="398a6-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="398a6-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="398a6-146">Der Integrations Kontovereinbarung-Wert des Host Identitäts Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="398a6-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="398a6-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="398a6-147">-HostPartner</span></span>
<span data-ttu-id="398a6-148">Gibt den Namen des Host Partners an.</span><span class="sxs-lookup"><span data-stu-id="398a6-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="398a6-149">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="398a6-149">-Metadata</span></span>
<span data-ttu-id="398a6-150">Gibt ein Metadaten-Objekt für die Vereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="398a6-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="398a6-151">-Name</span><span class="sxs-lookup"><span data-stu-id="398a6-151">-Name</span></span>
<span data-ttu-id="398a6-152">Gibt den Namen des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="398a6-152">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="398a6-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="398a6-153">-ResourceGroupName</span></span>
<span data-ttu-id="398a6-154">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="398a6-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="398a6-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="398a6-155">-Confirm</span></span>
<span data-ttu-id="398a6-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="398a6-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="398a6-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="398a6-157">-WhatIf</span></span>
<span data-ttu-id="398a6-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="398a6-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="398a6-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="398a6-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="398a6-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="398a6-160">CommonParameters</span></span>
<span data-ttu-id="398a6-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="398a6-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="398a6-162">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="398a6-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="398a6-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="398a6-163">INPUTS</span></span>

### <span data-ttu-id="398a6-164">System. String</span><span class="sxs-lookup"><span data-stu-id="398a6-164">System.String</span></span>

## <span data-ttu-id="398a6-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="398a6-165">OUTPUTS</span></span>

### <span data-ttu-id="398a6-166">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="398a6-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="398a6-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="398a6-167">NOTES</span></span>

## <span data-ttu-id="398a6-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="398a6-168">RELATED LINKS</span></span>

[<span data-ttu-id="398a6-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="398a6-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="398a6-170">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="398a6-170">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="398a6-171">Satz-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="398a6-171">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


