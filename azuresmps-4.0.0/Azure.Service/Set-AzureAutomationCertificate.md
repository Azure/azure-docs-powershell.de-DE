---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: AE74024A-A12A-4EC4-AF6C-62F921EA2532
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b19d0bb0c95e9d489fe26c1cd74705318cedcf2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006634"
---
# <span data-ttu-id="8bb7f-101">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="8bb7f-101">Set-AzureAutomationCertificate</span></span>

## <span data-ttu-id="8bb7f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8bb7f-102">SYNOPSIS</span></span>

<span data-ttu-id="8bb7f-103">Ändert die Konfiguration eines Automatisierungs Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="8bb7f-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="8bb7f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bb7f-104">SYNTAX</span></span>

```
Set-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8bb7f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8bb7f-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="8bb7f-106">Das Cmdlet " **Satz-AzureAutomationCertificate** " ändert die Konfiguration eines Zertifikats in der Microsoft Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="8bb7f-106">The **Set-AzureAutomationCertificate** cmdlet modifies the configuration of a certificate in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="8bb7f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8bb7f-107">EXAMPLES</span></span>

### <span data-ttu-id="8bb7f-108">Beispiel 1: Aktualisieren eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="8bb7f-108">Example 1: Update a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="8bb7f-109">Diese Befehle aktualisieren ein vorhandenes Zertifikat mit dem Namen myCertificate in Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="8bb7f-109">These commands update an existing certificate named MyCertificate in Automation.</span></span>
<span data-ttu-id="8bb7f-110">Mit dem ersten Befehl wird das Kennwort für die Zertifikatdatei erstellt, das im zweiten Befehl zum Aktualisieren des Zertifikats verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8bb7f-110">The first command creates the password for the certificate file that is used in the second command that updates the certificate.</span></span>

## <span data-ttu-id="8bb7f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bb7f-111">PARAMETERS</span></span>

### <span data-ttu-id="8bb7f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8bb7f-112">-AutomationAccountName</span></span>
<span data-ttu-id="8bb7f-113">Gibt den Namen des Automatisierungs Kontos mit dem Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="8bb7f-113">Specifies the name of the Automation account with the certificate.</span></span>

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

### <span data-ttu-id="8bb7f-114">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8bb7f-114">-Description</span></span>
<span data-ttu-id="8bb7f-115">Gibt eine Beschreibung für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="8bb7f-115">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="8bb7f-116">-Exportierbar</span><span class="sxs-lookup"><span data-stu-id="8bb7f-116">-Exportable</span></span>
<span data-ttu-id="8bb7f-117">Gibt an, dass das Zertifikat exportiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="8bb7f-117">Indicates the certificate can be exported.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb7f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8bb7f-118">-Name</span></span>
<span data-ttu-id="8bb7f-119">Gibt den Namen des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="8bb7f-119">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="8bb7f-120">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="8bb7f-120">-Password</span></span>
<span data-ttu-id="8bb7f-121">Gibt das Kennwort für die Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="8bb7f-121">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="8bb7f-122">-Path</span><span class="sxs-lookup"><span data-stu-id="8bb7f-122">-Path</span></span>
<span data-ttu-id="8bb7f-123">Gibt den Pfad zu einer Skriptdatei an, die hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8bb7f-123">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="8bb7f-124">Die Datei kann "CER" oder ". pfx" sein.</span><span class="sxs-lookup"><span data-stu-id="8bb7f-124">The file can be .cer or .pfx.</span></span>

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

### <span data-ttu-id="8bb7f-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="8bb7f-125">-Profile</span></span>
<span data-ttu-id="8bb7f-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8bb7f-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8bb7f-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8bb7f-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8bb7f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb7f-128">CommonParameters</span></span>
<span data-ttu-id="8bb7f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bb7f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb7f-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bb7f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb7f-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8bb7f-131">INPUTS</span></span>

## <span data-ttu-id="8bb7f-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8bb7f-132">OUTPUTS</span></span>

### <span data-ttu-id="8bb7f-133">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="8bb7f-133">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="8bb7f-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="8bb7f-134">NOTES</span></span>

## <span data-ttu-id="8bb7f-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8bb7f-135">RELATED LINKS</span></span>

[<span data-ttu-id="8bb7f-136">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="8bb7f-136">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="8bb7f-137">Neu – AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="8bb7f-137">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="8bb7f-138">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="8bb7f-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)


