---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 3a504ba081852ff3bb84a6ace432b394a2b2b478
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370486"
---
# <span data-ttu-id="50156-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="50156-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="50156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50156-102">SYNOPSIS</span></span>
<span data-ttu-id="50156-103">Ruft Automatisierungszertifikate ab.</span><span class="sxs-lookup"><span data-stu-id="50156-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="50156-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50156-104">SYNTAX</span></span>

### <span data-ttu-id="50156-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="50156-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50156-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="50156-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50156-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50156-107">DESCRIPTION</span></span>
<span data-ttu-id="50156-108">Das **Cmdlet "Get-AzAutomationCertificate"** ruft mindestens ein Azure-Automatisierungszertifikat ab.</span><span class="sxs-lookup"><span data-stu-id="50156-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="50156-109">Dieses Cmdlet ruft standardmäßig alle Zertifikate ab.</span><span class="sxs-lookup"><span data-stu-id="50156-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="50156-110">Geben Sie den Namen eines Zertifikats an, um ein bestimmtes Zertifikat zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="50156-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="50156-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="50156-111">EXAMPLES</span></span>

### <span data-ttu-id="50156-112">Beispiel 1: Alle Zertifikate erhalten</span><span class="sxs-lookup"><span data-stu-id="50156-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="50156-113">Dieser Befehl ruft Metadaten für alle Zertifikate im Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="50156-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="50156-114">Beispiel 2: Erhalten eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="50156-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="50156-115">Dieser Befehl ruft Metadaten für das Zertifikat mit dem Namen "ContosoCertificate" ab.</span><span class="sxs-lookup"><span data-stu-id="50156-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="50156-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50156-116">PARAMETERS</span></span>

### <span data-ttu-id="50156-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="50156-117">-AutomationAccountName</span></span>
<span data-ttu-id="50156-118">Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet ein Zertifikat abruft.</span><span class="sxs-lookup"><span data-stu-id="50156-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50156-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50156-119">-DefaultProfile</span></span>
<span data-ttu-id="50156-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="50156-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50156-121">-Name</span><span class="sxs-lookup"><span data-stu-id="50156-121">-Name</span></span>
<span data-ttu-id="50156-122">Gibt den Namen eines abzurufenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="50156-122">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50156-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50156-123">-ResourceGroupName</span></span>
<span data-ttu-id="50156-124">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet ein Automatisierungszertifikat erhält.</span><span class="sxs-lookup"><span data-stu-id="50156-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50156-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50156-125">CommonParameters</span></span>
<span data-ttu-id="50156-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50156-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50156-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50156-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50156-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="50156-128">INPUTS</span></span>

### <span data-ttu-id="50156-129">System.String</span><span class="sxs-lookup"><span data-stu-id="50156-129">System.String</span></span>

## <span data-ttu-id="50156-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="50156-130">OUTPUTS</span></span>

### <span data-ttu-id="50156-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="50156-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="50156-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="50156-132">NOTES</span></span>

## <span data-ttu-id="50156-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="50156-133">RELATED LINKS</span></span>

[<span data-ttu-id="50156-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="50156-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="50156-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="50156-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="50156-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="50156-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


