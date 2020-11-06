---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 3d26bca20befc31edfa437c7d3f9bc5dfced2b7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479166"
---
# <span data-ttu-id="18dbb-101">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="18dbb-101">Get-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="18dbb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="18dbb-103">Ruft Integrations Kontozertifikate aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="18dbb-103">Gets integration account certificates from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18dbb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18dbb-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>]
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18dbb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18dbb-105">DESCRIPTION</span></span>
<span data-ttu-id="18dbb-106">Das Cmdlet " **Get-AzureRmIntegrationAccountCertificate** " ruft Integrations Kontozertifikate aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="18dbb-106">The **Get-AzureRmIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="18dbb-107">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Zertifikatsnamen an.</span><span class="sxs-lookup"><span data-stu-id="18dbb-107">Specify the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="18dbb-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="18dbb-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="18dbb-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="18dbb-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="18dbb-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="18dbb-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="18dbb-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="18dbb-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="18dbb-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18dbb-112">EXAMPLES</span></span>

### <span data-ttu-id="18dbb-113">Beispiel 1: Abrufen eines Integrations Kontozertifikats</span><span class="sxs-lookup"><span data-stu-id="18dbb-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="18dbb-114">Dieser Befehl ruft das Integrations Kontozertifikat mit dem Namen IntegrationAccountCertificate01 ab.</span><span class="sxs-lookup"><span data-stu-id="18dbb-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="18dbb-115">Beispiel 2: Abrufen von Integrations Kontozertifikaten nach dem Namen des Integrations Kontos</span><span class="sxs-lookup"><span data-stu-id="18dbb-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="18dbb-116">Dieser Befehl ruft die Integrations Kontozertifikate für das Integrations Konto mit dem Namen IntegrationAccount31 ab.</span><span class="sxs-lookup"><span data-stu-id="18dbb-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="18dbb-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="18dbb-117">PARAMETERS</span></span>

### <span data-ttu-id="18dbb-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="18dbb-118">-CertificateName</span></span>
<span data-ttu-id="18dbb-119">Gibt den Namen eines Integrations Kontozertifikats an.</span><span class="sxs-lookup"><span data-stu-id="18dbb-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="18dbb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="18dbb-120">-Name</span></span>
<span data-ttu-id="18dbb-121">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="18dbb-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="18dbb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18dbb-122">-ResourceGroupName</span></span>
<span data-ttu-id="18dbb-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="18dbb-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="18dbb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18dbb-124">-DefaultProfile</span></span>
<span data-ttu-id="18dbb-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="18dbb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18dbb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18dbb-126">CommonParameters</span></span>
<span data-ttu-id="18dbb-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18dbb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18dbb-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18dbb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18dbb-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18dbb-129">INPUTS</span></span>

## <span data-ttu-id="18dbb-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18dbb-130">OUTPUTS</span></span>

### <span data-ttu-id="18dbb-131">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="18dbb-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="18dbb-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="18dbb-132">NOTES</span></span>

## <span data-ttu-id="18dbb-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18dbb-133">RELATED LINKS</span></span>

[<span data-ttu-id="18dbb-134">Neu – AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="18dbb-134">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="18dbb-135">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="18dbb-135">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="18dbb-136">Satz-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="18dbb-136">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


