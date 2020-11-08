---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FDA8BAAA-7C37-4BCB-9C02-EB6296C09C2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 00904cc1b67c32bc3658c1c4f6e8b123a5601ff7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006428"
---
# <span data-ttu-id="f4875-101">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f4875-101">New-AzureAutomationCertificate</span></span>

## <span data-ttu-id="f4875-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4875-102">SYNOPSIS</span></span>

<span data-ttu-id="f4875-103">Erstellt ein Azure-Automatisierungs Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="f4875-103">Creates an Azure Automation certificate.</span></span>

## <span data-ttu-id="f4875-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4875-104">SYNTAX</span></span>

```
New-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>] -Path <String>
 [-Exportable] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f4875-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4875-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="f4875-106">Das Cmdlet **New-AzureAutomationCertificate** erstellt ein Zertifikat in Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f4875-106">The **New-AzureAutomationCertificate** cmdlet creates a certificate in Microsoft Azure Automation.</span></span>
<span data-ttu-id="f4875-107">Sie geben den Pfad zu einer Zertifikatsdatei an, die hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4875-107">You provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="f4875-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4875-108">EXAMPLES</span></span>

### <span data-ttu-id="f4875-109">Beispiel 1: Erstellen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="f4875-109">Example 1: Create a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> New-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="f4875-110">Mit diesen Befehlen wird ein Zertifikat in Azure Automation mit dem Namen "myCertificate" erstellt.</span><span class="sxs-lookup"><span data-stu-id="f4875-110">These commands create a certificate in Azure Automation named MyCertificate.</span></span>
<span data-ttu-id="f4875-111">Mit dem ersten Befehl wird das Kennwort für die Zertifikatdatei erstellt, das im zweiten Befehl zum Erstellen des Zertifikats verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f4875-111">The first command creates the password for the certificate file that is used in the second command that creates the certificate.</span></span>

## <span data-ttu-id="f4875-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4875-112">PARAMETERS</span></span>

### <span data-ttu-id="f4875-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f4875-113">-AutomationAccountName</span></span>
<span data-ttu-id="f4875-114">Gibt den Namen des Automatisierungs Kontos an, in dem das Zertifikat gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4875-114">Specifies the name of the Automation account the certificate will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4875-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4875-115">-Description</span></span>
<span data-ttu-id="f4875-116">Gibt eine Beschreibung für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="f4875-116">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="f4875-117">-Exportierbar</span><span class="sxs-lookup"><span data-stu-id="f4875-117">-Exportable</span></span>
<span data-ttu-id="f4875-118">Gibt an, dass das Zertifikat exportiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f4875-118">Indicates the certificate can be exported.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4875-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f4875-119">-Name</span></span>
<span data-ttu-id="f4875-120">Gibt einen Namen für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="f4875-120">Specifies a name for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4875-121">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="f4875-121">-Password</span></span>
<span data-ttu-id="f4875-122">Gibt das Kennwort für die Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="f4875-122">Specifies the password for the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4875-123">-Path</span><span class="sxs-lookup"><span data-stu-id="f4875-123">-Path</span></span>
<span data-ttu-id="f4875-124">Gibt den Pfad zu einer Skriptdatei an, die hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4875-124">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="f4875-125">Die Datei kann "CER" oder ". pfx" sein.</span><span class="sxs-lookup"><span data-stu-id="f4875-125">The file can be .cer or .pfx.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4875-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="f4875-126">-Profile</span></span>
<span data-ttu-id="f4875-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="f4875-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f4875-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f4875-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4875-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4875-129">CommonParameters</span></span>
<span data-ttu-id="f4875-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4875-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4875-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4875-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4875-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4875-132">INPUTS</span></span>

## <span data-ttu-id="f4875-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4875-133">OUTPUTS</span></span>

### <span data-ttu-id="f4875-134">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="f4875-134">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="f4875-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4875-135">NOTES</span></span>

## <span data-ttu-id="f4875-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4875-136">RELATED LINKS</span></span>

[<span data-ttu-id="f4875-137">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f4875-137">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="f4875-138">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f4875-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="f4875-139">Satz-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f4875-139">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


