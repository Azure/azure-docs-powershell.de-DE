---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
ms.openlocfilehash: ac0e5e89706e648d714e3f09ebad5dee7d7b4416
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459096"
---
# <span data-ttu-id="9366e-101">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="9366e-101">Set-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="9366e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9366e-102">SYNOPSIS</span></span>
<span data-ttu-id="9366e-103">Ändert einen Vertrag für ein Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="9366e-103">Modifies an integration account agreement.</span></span>

## <span data-ttu-id="9366e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9366e-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9366e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9366e-105">DESCRIPTION</span></span>
<span data-ttu-id="9366e-106">Das **Cmdlet Set-AzIntegrationAccountAgreement** ändert eine Vereinbarung für ein Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="9366e-106">The **Set-AzIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="9366e-107">Dieses Cmdlet gibt ein Objekt zurück, das den Vertrag für das Integrationskonto darstellt.</span><span class="sxs-lookup"><span data-stu-id="9366e-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="9366e-108">Geben Sie den Namen des Integrationskontos, den Namen der Ressourcengruppe und den Vertragsnamen an.</span><span class="sxs-lookup"><span data-stu-id="9366e-108">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="9366e-109">Werte der Vorlagenparameterdatei, die Sie in der Befehlszeile angeben, haben Vorrang vor Vorlagenparameterwerten in einem Vorlagenparameterobjekt.</span><span class="sxs-lookup"><span data-stu-id="9366e-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="9366e-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="9366e-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9366e-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="9366e-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9366e-112">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="9366e-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9366e-113">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="9366e-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9366e-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9366e-114">EXAMPLES</span></span>

### <span data-ttu-id="9366e-115">Beispiel 1: Aktualisieren einer Vereinbarung für ein Integrationskonto</span><span class="sxs-lookup"><span data-stu-id="9366e-115">Example 1: Update an integration account agreement</span></span>
```powershell
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

<span data-ttu-id="9366e-116">Mit diesem Befehl wird eine Vereinbarung für ein Integrationskonto in der angegebenen Azure-Ressourcengruppe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9366e-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="9366e-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9366e-117">Example 2</span></span>

<span data-ttu-id="9366e-118">Ändert einen Vertrag für ein Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="9366e-118">Modifies an integration account agreement.</span></span> <span data-ttu-id="9366e-119">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="9366e-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountAgreement -AgreementContentFilePath 'C:\temp\AgreementContent.json' -AgreementName 'IntegrationAccountAgreement06' -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Metadata <Object> -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="9366e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9366e-120">PARAMETERS</span></span>

### <span data-ttu-id="9366e-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="9366e-121">-AgreementContent</span></span>
<span data-ttu-id="9366e-122">Gibt Vertragsinhalt im JavaScript Object Notation (JSON)-Format für den Vertrag an.</span><span class="sxs-lookup"><span data-stu-id="9366e-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="9366e-123">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="9366e-123">-AgreementContentFilePath</span></span>
<span data-ttu-id="9366e-124">Gibt den Dateipfad des Vertragsinhalts für den Vertrag an.</span><span class="sxs-lookup"><span data-stu-id="9366e-124">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="9366e-125">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="9366e-125">-AgreementName</span></span>
<span data-ttu-id="9366e-126">Gibt den Namen des Vertrags für das Integrationskonto an.</span><span class="sxs-lookup"><span data-stu-id="9366e-126">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="9366e-127">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="9366e-127">-AgreementType</span></span>
<span data-ttu-id="9366e-128">Gibt den Vertragstyp für das Integrationskonto an.</span><span class="sxs-lookup"><span data-stu-id="9366e-128">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="9366e-129">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="9366e-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9366e-130">X12</span><span class="sxs-lookup"><span data-stu-id="9366e-130">X12</span></span> 
- <span data-ttu-id="9366e-131">AS2</span><span class="sxs-lookup"><span data-stu-id="9366e-131">AS2</span></span>
- <span data-ttu-id="9366e-132">Edifact</span><span class="sxs-lookup"><span data-stu-id="9366e-132">Edifact</span></span>

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

### <span data-ttu-id="9366e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9366e-133">-DefaultProfile</span></span>
<span data-ttu-id="9366e-134">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9366e-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9366e-135">-Force</span><span class="sxs-lookup"><span data-stu-id="9366e-135">-Force</span></span>
<span data-ttu-id="9366e-136">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="9366e-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9366e-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="9366e-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="9366e-138">Gibt einen Namensidentitätsqualifizierer für den Gastpartner an.</span><span class="sxs-lookup"><span data-stu-id="9366e-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="9366e-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="9366e-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="9366e-140">Der Wert für den Gastidentitätsqualifizierer für den Integrationskontovertrag.</span><span class="sxs-lookup"><span data-stu-id="9366e-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="9366e-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="9366e-141">-GuestPartner</span></span>
<span data-ttu-id="9366e-142">Gibt den Namen des Gastpartners an.</span><span class="sxs-lookup"><span data-stu-id="9366e-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="9366e-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="9366e-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="9366e-144">Gibt einen Namensidentitätsqualifizierer für den Hostpartner an.</span><span class="sxs-lookup"><span data-stu-id="9366e-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="9366e-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="9366e-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="9366e-146">Der Hostidentitätsqualifiziererwert für den Integrationskontovertrag.</span><span class="sxs-lookup"><span data-stu-id="9366e-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="9366e-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="9366e-147">-HostPartner</span></span>
<span data-ttu-id="9366e-148">Gibt den Namen des Hostpartners an.</span><span class="sxs-lookup"><span data-stu-id="9366e-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="9366e-149">-Metadata</span><span class="sxs-lookup"><span data-stu-id="9366e-149">-Metadata</span></span>
<span data-ttu-id="9366e-150">Gibt ein Metadatenobjekt für die Vereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="9366e-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="9366e-151">-Name</span><span class="sxs-lookup"><span data-stu-id="9366e-151">-Name</span></span>
<span data-ttu-id="9366e-152">Gibt den Namen eines Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="9366e-152">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="9366e-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9366e-153">-ResourceGroupName</span></span>
<span data-ttu-id="9366e-154">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9366e-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9366e-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9366e-155">-Confirm</span></span>
<span data-ttu-id="9366e-156">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9366e-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9366e-157">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9366e-157">-WhatIf</span></span>
<span data-ttu-id="9366e-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9366e-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9366e-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9366e-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9366e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9366e-160">CommonParameters</span></span>
<span data-ttu-id="9366e-161">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9366e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9366e-162">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9366e-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9366e-163">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9366e-163">INPUTS</span></span>

### <span data-ttu-id="9366e-164">System.String</span><span class="sxs-lookup"><span data-stu-id="9366e-164">System.String</span></span>

## <span data-ttu-id="9366e-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9366e-165">OUTPUTS</span></span>

### <span data-ttu-id="9366e-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="9366e-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="9366e-167">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9366e-167">NOTES</span></span>

## <span data-ttu-id="9366e-168">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9366e-168">RELATED LINKS</span></span>

[<span data-ttu-id="9366e-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="9366e-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="9366e-170">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="9366e-170">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="9366e-171">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="9366e-171">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)


