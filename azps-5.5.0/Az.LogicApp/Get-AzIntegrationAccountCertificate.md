---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 46927e25fb4e32aae9ea1870ef9eeaedd5efe008
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147644"
---
# <span data-ttu-id="522bb-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="522bb-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="522bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="522bb-102">SYNOPSIS</span></span>
<span data-ttu-id="522bb-103">Ruft Integrationskontozertifikate aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="522bb-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="522bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="522bb-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="522bb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="522bb-105">DESCRIPTION</span></span>
<span data-ttu-id="522bb-106">Das **Cmdlet "Get-AzIntegrationAccountCertificate"** ruft Integrationskontozertifikate aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="522bb-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="522bb-107">Geben Sie den Namen des Integrationskontos, den Ressourcengruppennamen und den Zertifikatnamen an.</span><span class="sxs-lookup"><span data-stu-id="522bb-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="522bb-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="522bb-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="522bb-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="522bb-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="522bb-110">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="522bb-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="522bb-111">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="522bb-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="522bb-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="522bb-112">EXAMPLES</span></span>

### <span data-ttu-id="522bb-113">Beispiel 1: Erhalten eines Zertifikats für ein Integrationskonto</span><span class="sxs-lookup"><span data-stu-id="522bb-113">Example 1: Get an integration account certificate</span></span>
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

<span data-ttu-id="522bb-114">Dieser Befehl ruft das Zertifikat für das Integrationskonto namens "IntegrationAccountCertificate01" ab.</span><span class="sxs-lookup"><span data-stu-id="522bb-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="522bb-115">Beispiel 2: Erhalten von Integrationskontozertifikaten über den Namen des Integrationskontos</span><span class="sxs-lookup"><span data-stu-id="522bb-115">Example 2: Get integration account certificates by integration account name</span></span>
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

<span data-ttu-id="522bb-116">Dieser Befehl ruft die Integrationskontozertifikate für das Integrationskonto namens "IntegrationAccount31" ab.</span><span class="sxs-lookup"><span data-stu-id="522bb-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="522bb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="522bb-117">PARAMETERS</span></span>

### <span data-ttu-id="522bb-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="522bb-118">-CertificateName</span></span>
<span data-ttu-id="522bb-119">Gibt den Namen eines Zertifikats für ein Integrationskonto an.</span><span class="sxs-lookup"><span data-stu-id="522bb-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="522bb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="522bb-120">-DefaultProfile</span></span>
<span data-ttu-id="522bb-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="522bb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="522bb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="522bb-122">-Name</span></span>
<span data-ttu-id="522bb-123">Gibt den Namen eines Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="522bb-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="522bb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="522bb-124">-ResourceGroupName</span></span>
<span data-ttu-id="522bb-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="522bb-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="522bb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="522bb-126">CommonParameters</span></span>
<span data-ttu-id="522bb-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="522bb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="522bb-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="522bb-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="522bb-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="522bb-129">INPUTS</span></span>

### <span data-ttu-id="522bb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="522bb-130">System.String</span></span>

## <span data-ttu-id="522bb-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="522bb-131">OUTPUTS</span></span>

### <span data-ttu-id="522bb-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="522bb-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="522bb-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="522bb-133">NOTES</span></span>

## <span data-ttu-id="522bb-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="522bb-134">RELATED LINKS</span></span>

[<span data-ttu-id="522bb-135">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="522bb-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="522bb-136">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="522bb-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="522bb-137">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="522bb-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


