---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 82fb412cca4642881ff6a84ede1f2c722c6d5086
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947035"
---
# <span data-ttu-id="34957-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="34957-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="34957-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34957-102">SYNOPSIS</span></span>
<span data-ttu-id="34957-103">Erstellt einen Integrationskontovertrag.</span><span class="sxs-lookup"><span data-stu-id="34957-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="34957-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34957-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34957-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34957-105">DESCRIPTION</span></span>
<span data-ttu-id="34957-106">Das **Cmdlet New-AzIntegrationAccountAgreement** erstellt einen Integrationskontovertrag.</span><span class="sxs-lookup"><span data-stu-id="34957-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="34957-107">Dieses Cmdlet gibt ein -Objekt zurück, das den Integrationskontovertrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="34957-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="34957-108">Geben Sie den Namen des Integrationskontos, den Ressourcengruppennamen, den Vertragsnamen, den Typ, den Partnernamen, die Partnerqualifizierer und den Vertragsinhalt an.</span><span class="sxs-lookup"><span data-stu-id="34957-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="34957-109">Werte der Vorlagenparameterdatei, die Sie in der Befehlszeile angeben, haben Vorrang vor Vorlagenparameterwerten in einem Vorlagenparameterobjekt.</span><span class="sxs-lookup"><span data-stu-id="34957-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="34957-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="34957-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="34957-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="34957-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="34957-112">Um die Namen dynamischer Parameter zu ermitteln, geben Sie nach dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="34957-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="34957-113">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="34957-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="34957-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="34957-114">EXAMPLES</span></span>

### <span data-ttu-id="34957-115">Beispiel 1: Erstellen eines Integrationskontovertrags</span><span class="sxs-lookup"><span data-stu-id="34957-115">Example 1: Create a integration account agreement</span></span>
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

<span data-ttu-id="34957-116">Mit diesem Befehl wird eine Integrationskontovereinbarung in der angegebenen Azure-Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="34957-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="34957-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="34957-117">Example 2</span></span>

<span data-ttu-id="34957-118">Erstellt einen Integrationskontovertrag.</span><span class="sxs-lookup"><span data-stu-id="34957-118">Creates an integration account agreement.</span></span> <span data-ttu-id="34957-119">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="34957-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountAgreement -AgreementContent <String> -AgreementName 'IntegrationAccountAgreement06' -AgreementType X12 -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="34957-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="34957-120">PARAMETERS</span></span>

### <span data-ttu-id="34957-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="34957-121">-AgreementContent</span></span>
<span data-ttu-id="34957-122">Gibt den Vertragsinhalt im JavaScript-Objekt-Notation(JSON)-Format für den Vertrag an.</span><span class="sxs-lookup"><span data-stu-id="34957-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="34957-123">Geben Sie entweder diesen Parameter oder den *Parameter AgreementContentFilePath* an.</span><span class="sxs-lookup"><span data-stu-id="34957-123">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="34957-124">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="34957-124">-AgreementContentFilePath</span></span>
<span data-ttu-id="34957-125">Gibt den Dateipfad des Vertragsinhalts für den Vertrag an.</span><span class="sxs-lookup"><span data-stu-id="34957-125">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="34957-126">Geben Sie entweder diesen Parameter oder den *Parameter AgreementContent* an.</span><span class="sxs-lookup"><span data-stu-id="34957-126">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="34957-127">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="34957-127">-AgreementName</span></span>
<span data-ttu-id="34957-128">Gibt einen Namen für den Integrationskontovertrag an.</span><span class="sxs-lookup"><span data-stu-id="34957-128">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="34957-129">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="34957-129">-AgreementType</span></span>
<span data-ttu-id="34957-130">Gibt den Typ des Integrationskontovertrags an.</span><span class="sxs-lookup"><span data-stu-id="34957-130">Specifies the integration account agreement type.</span></span> <span data-ttu-id="34957-131">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="34957-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="34957-132">X12</span><span class="sxs-lookup"><span data-stu-id="34957-132">X12</span></span> 
- <span data-ttu-id="34957-133">AS2</span><span class="sxs-lookup"><span data-stu-id="34957-133">AS2</span></span>
- <span data-ttu-id="34957-134">Edifact</span><span class="sxs-lookup"><span data-stu-id="34957-134">Edifact</span></span>

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

### <span data-ttu-id="34957-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34957-135">-DefaultProfile</span></span>
<span data-ttu-id="34957-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="34957-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34957-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="34957-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="34957-138">Gibt einen Namens-Geschäftsidentitätsqualifizierer für den Gastpartner an.</span><span class="sxs-lookup"><span data-stu-id="34957-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="34957-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="34957-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="34957-140">Der Wert für den Gastidentitätsqualifizierer für das Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="34957-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="34957-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="34957-141">-GuestPartner</span></span>
<span data-ttu-id="34957-142">Gibt den Namen des Gastpartners an.</span><span class="sxs-lookup"><span data-stu-id="34957-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="34957-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="34957-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="34957-144">Gibt einen Namens-Geschäftsidentitätsqualifizierer für den Hostpartner an.</span><span class="sxs-lookup"><span data-stu-id="34957-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="34957-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="34957-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="34957-146">Der Hostidentitätsqualifiziererwert für integrationskontovereinbarung.</span><span class="sxs-lookup"><span data-stu-id="34957-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="34957-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="34957-147">-HostPartner</span></span>
<span data-ttu-id="34957-148">Gibt den Namen des Hostpartners an.</span><span class="sxs-lookup"><span data-stu-id="34957-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="34957-149">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="34957-149">-Metadata</span></span>
<span data-ttu-id="34957-150">Gibt ein Metadatenobjekt für die Vereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="34957-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="34957-151">-Name</span><span class="sxs-lookup"><span data-stu-id="34957-151">-Name</span></span>
<span data-ttu-id="34957-152">Gibt den Namen des Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="34957-152">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="34957-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34957-153">-ResourceGroupName</span></span>
<span data-ttu-id="34957-154">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="34957-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="34957-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="34957-155">-Confirm</span></span>
<span data-ttu-id="34957-156">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="34957-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34957-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34957-157">-WhatIf</span></span>
<span data-ttu-id="34957-158">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34957-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34957-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34957-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34957-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34957-160">CommonParameters</span></span>
<span data-ttu-id="34957-161">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34957-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34957-162">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34957-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34957-163">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="34957-163">INPUTS</span></span>

### <span data-ttu-id="34957-164">System.String</span><span class="sxs-lookup"><span data-stu-id="34957-164">System.String</span></span>

## <span data-ttu-id="34957-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="34957-165">OUTPUTS</span></span>

### <span data-ttu-id="34957-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="34957-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="34957-167">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="34957-167">NOTES</span></span>

## <span data-ttu-id="34957-168">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="34957-168">RELATED LINKS</span></span>

[<span data-ttu-id="34957-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="34957-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="34957-170">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="34957-170">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="34957-171">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="34957-171">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


