---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: eadd3052bb965b60bdaf377cd45fc014f25cac79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663479"
---
# <span data-ttu-id="901e3-101">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="901e3-101">Get-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="901e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="901e3-102">SYNOPSIS</span></span>
<span data-ttu-id="901e3-103">Ruft eine Integrations Kontovereinbarung ab.</span><span class="sxs-lookup"><span data-stu-id="901e3-103">Gets an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="901e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="901e3-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="901e3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="901e3-105">DESCRIPTION</span></span>
<span data-ttu-id="901e3-106">Das Cmdlet " **Get-AzureRmIntegrationAccountAgreement** " Ruft eine Integration-Kontovereinbarung aus einer Azure-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="901e3-106">The **Get-AzureRmIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="901e3-107">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Vertragsnamen an.</span><span class="sxs-lookup"><span data-stu-id="901e3-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="901e3-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="901e3-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="901e3-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="901e3-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="901e3-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="901e3-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="901e3-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="901e3-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="901e3-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="901e3-112">EXAMPLES</span></span>

### <span data-ttu-id="901e3-113">Beispiel 1: Abrufen einer Integrations Kontovereinbarung</span><span class="sxs-lookup"><span data-stu-id="901e3-113">Example 1: Get an integration account agreement</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06"
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

<span data-ttu-id="901e3-114">Dieser Befehl ruft eine Integrations Kontovereinbarung mit dem Namen IntegrationAccountAgreement06 ab.</span><span class="sxs-lookup"><span data-stu-id="901e3-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="901e3-115">Beispiel 2: Abrufen von Integrations Konto Vereinbarungen nach Ressourcengruppennamen</span><span class="sxs-lookup"><span data-stu-id="901e3-115">Example 2: Get integration account agreements by resource group name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="901e3-116">Dieser Befehl ruft die Integrations Konto Vereinbarungen nach Ressourcengruppennamen ab.</span><span class="sxs-lookup"><span data-stu-id="901e3-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="901e3-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="901e3-117">PARAMETERS</span></span>

### <span data-ttu-id="901e3-118">-Vertragsname</span><span class="sxs-lookup"><span data-stu-id="901e3-118">-AgreementName</span></span>
<span data-ttu-id="901e3-119">Gibt den Namen einer Integrations Kontovereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="901e3-119">Specifies the name of an integration account agreement.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901e3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="901e3-120">-DefaultProfile</span></span>
<span data-ttu-id="901e3-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="901e3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901e3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="901e3-122">-Name</span></span>
<span data-ttu-id="901e3-123">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="901e3-123">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901e3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="901e3-124">-ResourceGroupName</span></span>
<span data-ttu-id="901e3-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="901e3-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="901e3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="901e3-126">CommonParameters</span></span>
<span data-ttu-id="901e3-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="901e3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="901e3-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="901e3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="901e3-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="901e3-129">INPUTS</span></span>

### <span data-ttu-id="901e3-130">Keine</span><span class="sxs-lookup"><span data-stu-id="901e3-130">None</span></span>
<span data-ttu-id="901e3-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="901e3-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="901e3-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="901e3-132">OUTPUTS</span></span>

### <span data-ttu-id="901e3-133">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="901e3-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="901e3-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="901e3-134">NOTES</span></span>

## <span data-ttu-id="901e3-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="901e3-135">RELATED LINKS</span></span>

[<span data-ttu-id="901e3-136">Neu – AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="901e3-136">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="901e3-137">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="901e3-137">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="901e3-138">Satz-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="901e3-138">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


