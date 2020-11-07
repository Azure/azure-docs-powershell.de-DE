---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 7eaaabf374d4ee9b43477596df06f58593c6d1e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845359"
---
# <span data-ttu-id="ce677-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce677-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="ce677-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ce677-102">SYNOPSIS</span></span>
<span data-ttu-id="ce677-103">Ändert die Konfiguration eines Automatisierungs Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="ce677-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="ce677-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce677-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce677-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce677-105">DESCRIPTION</span></span>
<span data-ttu-id="ce677-106">Das Cmdlet " **Satz-AzAutomationCertificate** " ändert die Konfiguration eines Zertifikats in Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="ce677-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="ce677-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce677-107">EXAMPLES</span></span>

### <span data-ttu-id="ce677-108">Beispiel 1: Ändern eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="ce677-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ce677-109">Mit dem ersten Befehl wird ein nur-Text-Kennwort als sichere Zeichenfolge mithilfe des ConvertTo-SecureString-Cmdlets konvertiert.</span><span class="sxs-lookup"><span data-stu-id="ce677-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="ce677-110">Der Befehl speichert das Objekt in der $Password Variablen.</span><span class="sxs-lookup"><span data-stu-id="ce677-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="ce677-111">Der zweite Befehl ändert ein Zertifikat mit dem Namen ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="ce677-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="ce677-112">Der Befehl verwendet das in $Password gespeicherte Kennwort.</span><span class="sxs-lookup"><span data-stu-id="ce677-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="ce677-113">Der Befehl gibt den Kontonamen und den Pfad der Datei an, die er hochlädt.</span><span class="sxs-lookup"><span data-stu-id="ce677-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="ce677-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce677-114">PARAMETERS</span></span>

### <span data-ttu-id="ce677-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ce677-115">-AutomationAccountName</span></span>
<span data-ttu-id="ce677-116">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet ein Zertifikat geändert hat.</span><span class="sxs-lookup"><span data-stu-id="ce677-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="ce677-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce677-117">-DefaultProfile</span></span>
<span data-ttu-id="ce677-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ce677-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce677-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce677-119">-Description</span></span>
<span data-ttu-id="ce677-120">Gibt eine Beschreibung für das Zertifikat an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ce677-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ce677-121">-Exportierbar</span><span class="sxs-lookup"><span data-stu-id="ce677-121">-Exportable</span></span>
<span data-ttu-id="ce677-122">Gibt an, ob das Zertifikat exportiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ce677-122">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce677-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ce677-123">-Name</span></span>
<span data-ttu-id="ce677-124">Gibt den Namen des Zertifikats an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ce677-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ce677-125">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="ce677-125">-Password</span></span>
<span data-ttu-id="ce677-126">Gibt das Kennwort für die Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="ce677-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="ce677-127">-Path</span><span class="sxs-lookup"><span data-stu-id="ce677-127">-Path</span></span>
<span data-ttu-id="ce677-128">Gibt den Pfad zu einer Skriptdatei an, die hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce677-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="ce677-129">Die Datei kann eine CER-Datei oder eine PFX-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="ce677-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="ce677-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce677-130">-ResourceGroupName</span></span>
<span data-ttu-id="ce677-131">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet ein Zertifikat geändert hat.</span><span class="sxs-lookup"><span data-stu-id="ce677-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="ce677-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce677-132">CommonParameters</span></span>
<span data-ttu-id="ce677-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce677-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce677-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce677-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce677-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ce677-135">INPUTS</span></span>

### <span data-ttu-id="ce677-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ce677-136">System.String</span></span>

### <span data-ttu-id="ce677-137">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="ce677-137">System.Security.SecureString</span></span>

### <span data-ttu-id="ce677-138">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ce677-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ce677-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ce677-139">OUTPUTS</span></span>

### <span data-ttu-id="ce677-140">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="ce677-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="ce677-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce677-141">NOTES</span></span>

## <span data-ttu-id="ce677-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ce677-142">RELATED LINKS</span></span>

[<span data-ttu-id="ce677-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce677-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="ce677-144">Neu – AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce677-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="ce677-145">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce677-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


