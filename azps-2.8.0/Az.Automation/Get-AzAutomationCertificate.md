---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 70b92cd7762b42fba7ae890cd22b529ba80318ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658079"
---
# <span data-ttu-id="b1f7d-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1f7d-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="b1f7d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f7d-103">Ruft Automatisierungs Zertifikate ab.</span><span class="sxs-lookup"><span data-stu-id="b1f7d-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="b1f7d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1f7d-104">SYNTAX</span></span>

### <span data-ttu-id="b1f7d-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1f7d-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1f7d-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="b1f7d-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1f7d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1f7d-107">DESCRIPTION</span></span>
<span data-ttu-id="b1f7d-108">Das Cmdlet " **Get-AzAutomationCertificate** " ruft mindestens ein Azure-Automatisierungs Zertifikat ab.</span><span class="sxs-lookup"><span data-stu-id="b1f7d-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="b1f7d-109">Standardmäßig werden mit diesem Cmdlet alle Zertifikate abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b1f7d-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="b1f7d-110">Geben Sie den Namen eines Zertifikats an, um ein bestimmtes Zertifikat zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b1f7d-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="b1f7d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1f7d-111">EXAMPLES</span></span>

### <span data-ttu-id="b1f7d-112">Beispiel 1: Abrufen aller Zertifikate</span><span class="sxs-lookup"><span data-stu-id="b1f7d-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="b1f7d-113">Dieser Befehl ruft Metadaten für alle Zertifikate im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="b1f7d-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b1f7d-114">Beispiel 2: Abrufen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="b1f7d-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="b1f7d-115">Dieser Befehl ruft Metadaten für das Zertifikat mit dem Namen ContosoCertificate ab.</span><span class="sxs-lookup"><span data-stu-id="b1f7d-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="b1f7d-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1f7d-116">PARAMETERS</span></span>

### <span data-ttu-id="b1f7d-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b1f7d-117">-AutomationAccountName</span></span>
<span data-ttu-id="b1f7d-118">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet ein Zertifikat abruft.</span><span class="sxs-lookup"><span data-stu-id="b1f7d-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="b1f7d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f7d-119">-DefaultProfile</span></span>
<span data-ttu-id="b1f7d-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b1f7d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1f7d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b1f7d-121">-Name</span></span>
<span data-ttu-id="b1f7d-122">Gibt den Namen eines Zertifikats an, das abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1f7d-122">Specifies the name of a certificate to retrieve.</span></span>

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

### <span data-ttu-id="b1f7d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1f7d-123">-ResourceGroupName</span></span>
<span data-ttu-id="b1f7d-124">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet ein Automatisierungs Zertifikat erhält.</span><span class="sxs-lookup"><span data-stu-id="b1f7d-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="b1f7d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f7d-125">CommonParameters</span></span>
<span data-ttu-id="b1f7d-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1f7d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f7d-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1f7d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f7d-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1f7d-128">INPUTS</span></span>

### <span data-ttu-id="b1f7d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b1f7d-129">System.String</span></span>

## <span data-ttu-id="b1f7d-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1f7d-130">OUTPUTS</span></span>

### <span data-ttu-id="b1f7d-131">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="b1f7d-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="b1f7d-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1f7d-132">NOTES</span></span>

## <span data-ttu-id="b1f7d-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1f7d-133">RELATED LINKS</span></span>

[<span data-ttu-id="b1f7d-134">Neu – AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1f7d-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="b1f7d-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1f7d-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="b1f7d-136">Satz-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1f7d-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


