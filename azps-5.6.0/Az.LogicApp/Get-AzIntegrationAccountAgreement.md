---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 9ff2858eb032ff4ff4cc78e803b15f385fc71b7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950160"
---
# <span data-ttu-id="4080a-101">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="4080a-101">Get-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="4080a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4080a-102">SYNOPSIS</span></span>
<span data-ttu-id="4080a-103">Ruft einen Integrationskontovertrag ab.</span><span class="sxs-lookup"><span data-stu-id="4080a-103">Gets an integration account agreement.</span></span>

## <span data-ttu-id="4080a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4080a-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4080a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4080a-105">DESCRIPTION</span></span>
<span data-ttu-id="4080a-106">Das **Get-AzIntegrationAccountAgreement-Cmdlet** erhält einen Integrationskontovertrag von einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4080a-106">The **Get-AzIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="4080a-107">Geben Sie den Namen des Integrationskontos, den Ressourcengruppennamen und den Vertragsnamen an.</span><span class="sxs-lookup"><span data-stu-id="4080a-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="4080a-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="4080a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4080a-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="4080a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4080a-110">Um die Namen dynamischer Parameter zu ermitteln, geben Sie nach dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="4080a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4080a-111">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="4080a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4080a-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4080a-112">EXAMPLES</span></span>

### <span data-ttu-id="4080a-113">Beispiel 1: Erhalten eines Integrationskontovertrags</span><span class="sxs-lookup"><span data-stu-id="4080a-113">Example 1: Get an integration account agreement</span></span>
```
PS C:\>Get-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="4080a-114">Dieser Befehl ruft einen Integrationskontovertrag mit dem Namen IntegrationAccountAgreement06 ab.</span><span class="sxs-lookup"><span data-stu-id="4080a-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="4080a-115">Beispiel 2: Erhalten von Integrationskontovereinbarungen nach Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="4080a-115">Example 2: Get integration account agreements by resource group name</span></span>
```
PS C:\>Get-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="4080a-116">Dieser Befehl ruft die Integrationskontovereinbarungen nach Ressourcengruppennamen ab.</span><span class="sxs-lookup"><span data-stu-id="4080a-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="4080a-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4080a-117">PARAMETERS</span></span>

### <span data-ttu-id="4080a-118">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="4080a-118">-AgreementName</span></span>
<span data-ttu-id="4080a-119">Gibt den Namen eines Integrationskontovertrags an.</span><span class="sxs-lookup"><span data-stu-id="4080a-119">Specifies the name of an integration account agreement.</span></span>

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

### <span data-ttu-id="4080a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4080a-120">-DefaultProfile</span></span>
<span data-ttu-id="4080a-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4080a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4080a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4080a-122">-Name</span></span>
<span data-ttu-id="4080a-123">Gibt den Namen eines Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="4080a-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4080a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4080a-124">-ResourceGroupName</span></span>
<span data-ttu-id="4080a-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4080a-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4080a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4080a-126">CommonParameters</span></span>
<span data-ttu-id="4080a-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4080a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4080a-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4080a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4080a-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4080a-129">INPUTS</span></span>

### <span data-ttu-id="4080a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4080a-130">System.String</span></span>

## <span data-ttu-id="4080a-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4080a-131">OUTPUTS</span></span>

### <span data-ttu-id="4080a-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="4080a-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="4080a-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4080a-133">NOTES</span></span>

## <span data-ttu-id="4080a-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4080a-134">RELATED LINKS</span></span>

[<span data-ttu-id="4080a-135">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="4080a-135">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="4080a-136">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="4080a-136">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="4080a-137">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="4080a-137">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


