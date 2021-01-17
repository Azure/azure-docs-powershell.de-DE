---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 46927e25fb4e32aae9ea1870ef9eeaedd5efe008
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472325"
---
# <span data-ttu-id="3f6ce-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="3f6ce-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="3f6ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f6ce-102">SYNOPSIS</span></span>
<span data-ttu-id="3f6ce-103">Ruft Integrationskontozertifikate aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="3f6ce-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="3f6ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f6ce-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f6ce-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f6ce-105">DESCRIPTION</span></span>
<span data-ttu-id="3f6ce-106">Das **Cmdlet "Get-AzIntegrationAccountCertificate"** ruft Integrationskontozertifikate aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="3f6ce-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="3f6ce-107">Geben Sie den Namen des Integrationskontos, den Ressourcengruppennamen und den Zertifikatnamen an.</span><span class="sxs-lookup"><span data-stu-id="3f6ce-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="3f6ce-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="3f6ce-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3f6ce-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="3f6ce-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3f6ce-110">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="3f6ce-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3f6ce-111">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="3f6ce-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3f6ce-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f6ce-112">EXAMPLES</span></span>

### <span data-ttu-id="3f6ce-113">Beispiel 1: Erhalten eines Zertifikats für ein Integrationskonto</span><span class="sxs-lookup"><span data-stu-id="3f6ce-113">Example 1: Get an integration account certificate</span></span>
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

<span data-ttu-id="3f6ce-114">Dieser Befehl ruft das Zertifikat für das Integrationskonto namens "IntegrationAccountCertificate01" ab.</span><span class="sxs-lookup"><span data-stu-id="3f6ce-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="3f6ce-115">Beispiel 2: Erhalten von Integrationskontozertifikaten über den Namen des Integrationskontos</span><span class="sxs-lookup"><span data-stu-id="3f6ce-115">Example 2: Get integration account certificates by integration account name</span></span>
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

<span data-ttu-id="3f6ce-116">Dieser Befehl ruft die Integrationskontozertifikate für das Integrationskonto namens "IntegrationAccount31" ab.</span><span class="sxs-lookup"><span data-stu-id="3f6ce-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="3f6ce-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f6ce-117">PARAMETERS</span></span>

### <span data-ttu-id="3f6ce-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="3f6ce-118">-CertificateName</span></span>
<span data-ttu-id="3f6ce-119">Gibt den Namen eines Zertifikats für ein Integrationskonto an.</span><span class="sxs-lookup"><span data-stu-id="3f6ce-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="3f6ce-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f6ce-120">-DefaultProfile</span></span>
<span data-ttu-id="3f6ce-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3f6ce-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f6ce-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3f6ce-122">-Name</span></span>
<span data-ttu-id="3f6ce-123">Gibt den Namen eines Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="3f6ce-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="3f6ce-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f6ce-124">-ResourceGroupName</span></span>
<span data-ttu-id="3f6ce-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3f6ce-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3f6ce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f6ce-126">CommonParameters</span></span>
<span data-ttu-id="3f6ce-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f6ce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f6ce-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f6ce-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f6ce-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f6ce-129">INPUTS</span></span>

### <span data-ttu-id="3f6ce-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3f6ce-130">System.String</span></span>

## <span data-ttu-id="3f6ce-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f6ce-131">OUTPUTS</span></span>

### <span data-ttu-id="3f6ce-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="3f6ce-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="3f6ce-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3f6ce-133">NOTES</span></span>

## <span data-ttu-id="3f6ce-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3f6ce-134">RELATED LINKS</span></span>

[<span data-ttu-id="3f6ce-135">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="3f6ce-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="3f6ce-136">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="3f6ce-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="3f6ce-137">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="3f6ce-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


