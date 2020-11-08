---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: c80eb16f840fb6d590c139a6ec4b30d73584b741
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005180"
---
# <span data-ttu-id="3d27e-101">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3d27e-101">New-AzAutomationCertificate</span></span>

## <span data-ttu-id="3d27e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d27e-102">SYNOPSIS</span></span>
<span data-ttu-id="3d27e-103">Erstellt ein Automatisierungs Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="3d27e-103">Creates an Automation certificate.</span></span>

## <span data-ttu-id="3d27e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d27e-104">SYNTAX</span></span>

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d27e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d27e-105">DESCRIPTION</span></span>
<span data-ttu-id="3d27e-106">Das Cmdlet **New-AzAutomationCertificate** erstellt ein Zertifikat in Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="3d27e-106">The **New-AzAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="3d27e-107">Geben Sie den Pfad zu einer Zertifikatsdatei an, die hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d27e-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="3d27e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d27e-108">EXAMPLES</span></span>

### <span data-ttu-id="3d27e-109">Beispiel 1: Erstellen eines neuen Zertifikats</span><span class="sxs-lookup"><span data-stu-id="3d27e-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3d27e-110">Mit dem ersten Befehl wird ein nur-Text-Kennwort als sichere Zeichenfolge mithilfe des ConvertTo-SecureString-Cmdlets konvertiert.</span><span class="sxs-lookup"><span data-stu-id="3d27e-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="3d27e-111">Der Befehl speichert das Objekt in der $Password Variablen.</span><span class="sxs-lookup"><span data-stu-id="3d27e-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="3d27e-112">Der zweite Befehl erstellt ein Zertifikat mit dem Namen ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="3d27e-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="3d27e-113">Der Befehl verwendet das in $Password gespeicherte Kennwort.</span><span class="sxs-lookup"><span data-stu-id="3d27e-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="3d27e-114">Der Befehl gibt den Kontonamen und den Pfad der Datei an, die er hochlädt.</span><span class="sxs-lookup"><span data-stu-id="3d27e-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="3d27e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d27e-115">PARAMETERS</span></span>

### <span data-ttu-id="3d27e-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3d27e-116">-AutomationAccountName</span></span>
<span data-ttu-id="3d27e-117">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet das Zertifikat speichert.</span><span class="sxs-lookup"><span data-stu-id="3d27e-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="3d27e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d27e-118">-DefaultProfile</span></span>
<span data-ttu-id="3d27e-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3d27e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d27e-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d27e-120">-Description</span></span>
<span data-ttu-id="3d27e-121">Gibt eine Beschreibung für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="3d27e-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="3d27e-122">-Exportierbar</span><span class="sxs-lookup"><span data-stu-id="3d27e-122">-Exportable</span></span>
<span data-ttu-id="3d27e-123">Gibt an, ob das Zertifikat exportiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3d27e-123">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d27e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3d27e-124">-Name</span></span>
<span data-ttu-id="3d27e-125">Gibt den Namen des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="3d27e-125">Specifies the name for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d27e-126">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="3d27e-126">-Password</span></span>
<span data-ttu-id="3d27e-127">Gibt das Kennwort für die Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="3d27e-127">Specifies the password for the certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d27e-128">-Path</span><span class="sxs-lookup"><span data-stu-id="3d27e-128">-Path</span></span>
<span data-ttu-id="3d27e-129">Gibt den Pfad zu einer Skriptdatei an, die von diesem Cmdlet hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="3d27e-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="3d27e-130">Die Datei kann eine CER-oder PFX-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="3d27e-130">The file can be a .cer or a .pfx file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d27e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d27e-131">-ResourceGroupName</span></span>
<span data-ttu-id="3d27e-132">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet ein Zertifikat erstellt.</span><span class="sxs-lookup"><span data-stu-id="3d27e-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="3d27e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d27e-133">CommonParameters</span></span>
<span data-ttu-id="3d27e-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d27e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d27e-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d27e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d27e-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d27e-136">INPUTS</span></span>

### <span data-ttu-id="3d27e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3d27e-137">System.String</span></span>

### <span data-ttu-id="3d27e-138">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="3d27e-138">System.Security.SecureString</span></span>

### <span data-ttu-id="3d27e-139">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="3d27e-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3d27e-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d27e-140">OUTPUTS</span></span>

### <span data-ttu-id="3d27e-141">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="3d27e-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="3d27e-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d27e-142">NOTES</span></span>

<span data-ttu-id="3d27e-143">Dieser Befehl sollte auf einem Computer ausgeführt werden, dessen Administrator Sie sind, sowie in einer erhöhten PowerShell-Sitzung. bevor das Zertifikat hochgeladen wird, verwendet dieses Cmdlet den lokalen X. 509-Speicher, um den Fingerabdruck und den Schlüssel abzurufen, und wenn dieses Cmdlet außerhalb einer erhöhten PowerShell-Sitzung ausgeführt wird, wird der Fehler "Zugriff verweigert" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3d27e-143">This command should be run on a machine that you are an administrator of, as well as in an elevated PowerShell session; before the certificate is uploaded, this cmdlet uses the local X.509 store to retrieve the thumbprint and key, and if this cmdlet is run outside of an elevated PowerShell session, you will receive an "Access denied" error.</span></span>

## <span data-ttu-id="3d27e-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d27e-144">RELATED LINKS</span></span>

[<span data-ttu-id="3d27e-145">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3d27e-145">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="3d27e-146">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3d27e-146">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="3d27e-147">Satz-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3d27e-147">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


