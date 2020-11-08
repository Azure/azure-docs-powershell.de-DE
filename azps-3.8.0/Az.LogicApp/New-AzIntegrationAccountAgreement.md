---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: ee8eda56b5a84c6ddc00a1c5f94509c5da13874d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004542"
---
# <span data-ttu-id="dff64-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="dff64-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="dff64-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dff64-102">SYNOPSIS</span></span>
<span data-ttu-id="dff64-103">Erstellt eine Integrations Kontovereinbarung.</span><span class="sxs-lookup"><span data-stu-id="dff64-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="dff64-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dff64-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dff64-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dff64-105">DESCRIPTION</span></span>
<span data-ttu-id="dff64-106">Das Cmdlet **New-AzIntegrationAccountAgreement** erstellt eine Integrations Kontovereinbarung.</span><span class="sxs-lookup"><span data-stu-id="dff64-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="dff64-107">Dieses Cmdlet gibt ein Objekt zurück, das die Integrations Kontovereinbarung darstellt.</span><span class="sxs-lookup"><span data-stu-id="dff64-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="dff64-108">Geben Sie den Namen des Integrations Kontos, den Namen der Ressourcengruppe, den Namen der Vereinbarung, den Typ, den Partnernamen, die Partner Qualifizierer und den Vertragsinhalt an.</span><span class="sxs-lookup"><span data-stu-id="dff64-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="dff64-109">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="dff64-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="dff64-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="dff64-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="dff64-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="dff64-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="dff64-112">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="dff64-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="dff64-113">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="dff64-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="dff64-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dff64-114">EXAMPLES</span></span>

### <span data-ttu-id="dff64-115">Beispiel 1: Erstellen einer Integrations Kontovereinbarung</span><span class="sxs-lookup"><span data-stu-id="dff64-115">Example 1: Create a integration account agreement</span></span>
```
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

<span data-ttu-id="dff64-116">Mit diesem Befehl wird eine Integration-Kontovereinbarung in der angegebenen Azure-Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="dff64-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="dff64-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="dff64-117">PARAMETERS</span></span>

### <span data-ttu-id="dff64-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="dff64-118">-AgreementContent</span></span>
<span data-ttu-id="dff64-119">Gibt den Vertragsinhalt im JSON-Format (JavaScript Object Notation) für die Vereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="dff64-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="dff64-120">Geben Sie entweder diesen Parameter oder den *AgreementContentFilePath* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="dff64-120">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="dff64-121">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="dff64-121">-AgreementContentFilePath</span></span>
<span data-ttu-id="dff64-122">Gibt den Dateipfad der Vereinbarungs Inhalte an.</span><span class="sxs-lookup"><span data-stu-id="dff64-122">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="dff64-123">Geben Sie entweder diesen Parameter oder den *AgreementContent* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="dff64-123">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="dff64-124">-Vertragsname</span><span class="sxs-lookup"><span data-stu-id="dff64-124">-AgreementName</span></span>
<span data-ttu-id="dff64-125">Gibt einen Namen für die Integrations Kontovereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="dff64-125">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="dff64-126">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="dff64-126">-AgreementType</span></span>
<span data-ttu-id="dff64-127">Gibt den Typ der Integrations Kontovereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="dff64-127">Specifies the integration account agreement type.</span></span> <span data-ttu-id="dff64-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="dff64-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dff64-129">X12</span><span class="sxs-lookup"><span data-stu-id="dff64-129">X12</span></span> 
- <span data-ttu-id="dff64-130">AS2</span><span class="sxs-lookup"><span data-stu-id="dff64-130">AS2</span></span>
- <span data-ttu-id="dff64-131">EDIFACT</span><span class="sxs-lookup"><span data-stu-id="dff64-131">Edifact</span></span>

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

### <span data-ttu-id="dff64-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dff64-132">-DefaultProfile</span></span>
<span data-ttu-id="dff64-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dff64-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dff64-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="dff64-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="dff64-135">Gibt einen Namen Business Identity Qualifier für den Gast Partner an.</span><span class="sxs-lookup"><span data-stu-id="dff64-135">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="dff64-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="dff64-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="dff64-137">Der Integrations Konto-Vereinbarungs Wert des Gast Identitäts Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="dff64-137">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="dff64-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="dff64-138">-GuestPartner</span></span>
<span data-ttu-id="dff64-139">Gibt den Namen des Gast Partners an.</span><span class="sxs-lookup"><span data-stu-id="dff64-139">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="dff64-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="dff64-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="dff64-141">Gibt einen Namen Business Identity Qualifier für den Host Partner an.</span><span class="sxs-lookup"><span data-stu-id="dff64-141">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="dff64-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="dff64-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="dff64-143">Der Integrations Kontovereinbarung-Wert des Host Identitäts Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="dff64-143">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="dff64-144">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="dff64-144">-HostPartner</span></span>
<span data-ttu-id="dff64-145">Gibt den Namen des Host Partners an.</span><span class="sxs-lookup"><span data-stu-id="dff64-145">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="dff64-146">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="dff64-146">-Metadata</span></span>
<span data-ttu-id="dff64-147">Gibt ein Metadaten-Objekt für die Vereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="dff64-147">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="dff64-148">-Name</span><span class="sxs-lookup"><span data-stu-id="dff64-148">-Name</span></span>
<span data-ttu-id="dff64-149">Gibt den Namen des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="dff64-149">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="dff64-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dff64-150">-ResourceGroupName</span></span>
<span data-ttu-id="dff64-151">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="dff64-151">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="dff64-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dff64-152">-Confirm</span></span>
<span data-ttu-id="dff64-153">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dff64-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dff64-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dff64-154">-WhatIf</span></span>
<span data-ttu-id="dff64-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dff64-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dff64-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dff64-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dff64-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dff64-157">CommonParameters</span></span>
<span data-ttu-id="dff64-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dff64-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dff64-159">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dff64-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dff64-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dff64-160">INPUTS</span></span>

### <span data-ttu-id="dff64-161">System. String</span><span class="sxs-lookup"><span data-stu-id="dff64-161">System.String</span></span>

## <span data-ttu-id="dff64-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dff64-162">OUTPUTS</span></span>

### <span data-ttu-id="dff64-163">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="dff64-163">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="dff64-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="dff64-164">NOTES</span></span>

## <span data-ttu-id="dff64-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dff64-165">RELATED LINKS</span></span>

[<span data-ttu-id="dff64-166">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="dff64-166">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="dff64-167">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="dff64-167">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="dff64-168">Satz-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="dff64-168">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


