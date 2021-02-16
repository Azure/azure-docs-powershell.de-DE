---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 3a504ba081852ff3bb84a6ace432b394a2b2b478
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168460"
---
# <span data-ttu-id="bbf55-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bbf55-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="bbf55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbf55-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf55-103">Ruft Automatisierungszertifikate ab.</span><span class="sxs-lookup"><span data-stu-id="bbf55-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="bbf55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bbf55-104">SYNTAX</span></span>

### <span data-ttu-id="bbf55-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="bbf55-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbf55-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="bbf55-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbf55-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bbf55-107">DESCRIPTION</span></span>
<span data-ttu-id="bbf55-108">Das **Cmdlet "Get-AzAutomationCertificate"** ruft mindestens ein Azure-Automatisierungszertifikat ab.</span><span class="sxs-lookup"><span data-stu-id="bbf55-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="bbf55-109">Dieses Cmdlet ruft standardmäßig alle Zertifikate ab.</span><span class="sxs-lookup"><span data-stu-id="bbf55-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="bbf55-110">Geben Sie den Namen eines Zertifikats an, um ein bestimmtes Zertifikat zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bbf55-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="bbf55-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bbf55-111">EXAMPLES</span></span>

### <span data-ttu-id="bbf55-112">Beispiel 1: Alle Zertifikate erhalten</span><span class="sxs-lookup"><span data-stu-id="bbf55-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="bbf55-113">Dieser Befehl ruft Metadaten für alle Zertifikate im Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="bbf55-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="bbf55-114">Beispiel 2: Erhalten eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="bbf55-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="bbf55-115">Dieser Befehl ruft Metadaten für das Zertifikat mit dem Namen "ContosoCertificate" ab.</span><span class="sxs-lookup"><span data-stu-id="bbf55-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="bbf55-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbf55-116">PARAMETERS</span></span>

### <span data-ttu-id="bbf55-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bbf55-117">-AutomationAccountName</span></span>
<span data-ttu-id="bbf55-118">Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet ein Zertifikat abruft.</span><span class="sxs-lookup"><span data-stu-id="bbf55-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="bbf55-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf55-119">-DefaultProfile</span></span>
<span data-ttu-id="bbf55-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bbf55-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbf55-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bbf55-121">-Name</span></span>
<span data-ttu-id="bbf55-122">Gibt den Namen eines abzurufenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="bbf55-122">Specifies the name of a certificate to retrieve.</span></span>

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

### <span data-ttu-id="bbf55-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbf55-123">-ResourceGroupName</span></span>
<span data-ttu-id="bbf55-124">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet ein Automatisierungszertifikat erhält.</span><span class="sxs-lookup"><span data-stu-id="bbf55-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="bbf55-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf55-125">CommonParameters</span></span>
<span data-ttu-id="bbf55-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbf55-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf55-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbf55-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf55-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bbf55-128">INPUTS</span></span>

### <span data-ttu-id="bbf55-129">System.String</span><span class="sxs-lookup"><span data-stu-id="bbf55-129">System.String</span></span>

## <span data-ttu-id="bbf55-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bbf55-130">OUTPUTS</span></span>

### <span data-ttu-id="bbf55-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="bbf55-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="bbf55-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bbf55-132">NOTES</span></span>

## <span data-ttu-id="bbf55-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bbf55-133">RELATED LINKS</span></span>

[<span data-ttu-id="bbf55-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bbf55-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="bbf55-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bbf55-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="bbf55-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bbf55-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


