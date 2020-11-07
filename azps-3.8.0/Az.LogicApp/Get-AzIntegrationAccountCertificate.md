---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 46927e25fb4e32aae9ea1870ef9eeaedd5efe008
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846003"
---
# <span data-ttu-id="71085-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="71085-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="71085-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71085-102">SYNOPSIS</span></span>
<span data-ttu-id="71085-103">Ruft Integrations Kontozertifikate aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="71085-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="71085-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71085-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71085-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71085-105">DESCRIPTION</span></span>
<span data-ttu-id="71085-106">Das Cmdlet " **Get-AzIntegrationAccountCertificate** " ruft Integrations Kontozertifikate aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="71085-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="71085-107">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Zertifikatsnamen an.</span><span class="sxs-lookup"><span data-stu-id="71085-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="71085-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="71085-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="71085-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="71085-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="71085-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="71085-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="71085-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="71085-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="71085-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71085-112">EXAMPLES</span></span>

### <span data-ttu-id="71085-113">Beispiel 1: Abrufen eines Integrations Kontozertifikats</span><span class="sxs-lookup"><span data-stu-id="71085-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="71085-114">Dieser Befehl ruft das Integrations Kontozertifikat mit dem Namen IntegrationAccountCertificate01 ab.</span><span class="sxs-lookup"><span data-stu-id="71085-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="71085-115">Beispiel 2: Abrufen von Integrations Kontozertifikaten nach dem Namen des Integrations Kontos</span><span class="sxs-lookup"><span data-stu-id="71085-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="71085-116">Dieser Befehl ruft die Integrations Kontozertifikate für das Integrations Konto mit dem Namen IntegrationAccount31 ab.</span><span class="sxs-lookup"><span data-stu-id="71085-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="71085-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="71085-117">PARAMETERS</span></span>

### <span data-ttu-id="71085-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="71085-118">-CertificateName</span></span>
<span data-ttu-id="71085-119">Gibt den Namen eines Integrations Kontozertifikats an.</span><span class="sxs-lookup"><span data-stu-id="71085-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="71085-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71085-120">-DefaultProfile</span></span>
<span data-ttu-id="71085-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="71085-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71085-122">-Name</span><span class="sxs-lookup"><span data-stu-id="71085-122">-Name</span></span>
<span data-ttu-id="71085-123">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="71085-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="71085-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71085-124">-ResourceGroupName</span></span>
<span data-ttu-id="71085-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="71085-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="71085-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71085-126">CommonParameters</span></span>
<span data-ttu-id="71085-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71085-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71085-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71085-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71085-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71085-129">INPUTS</span></span>

### <span data-ttu-id="71085-130">System. String</span><span class="sxs-lookup"><span data-stu-id="71085-130">System.String</span></span>

## <span data-ttu-id="71085-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71085-131">OUTPUTS</span></span>

### <span data-ttu-id="71085-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="71085-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="71085-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="71085-133">NOTES</span></span>

## <span data-ttu-id="71085-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71085-134">RELATED LINKS</span></span>

[<span data-ttu-id="71085-135">Neu – AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="71085-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="71085-136">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="71085-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="71085-137">Satz-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="71085-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


