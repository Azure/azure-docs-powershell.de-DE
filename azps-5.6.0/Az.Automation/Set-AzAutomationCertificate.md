---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 80a33fe4664e4c7814db6774e7cd427dd9a2c87e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921480"
---
# <span data-ttu-id="fdb2f-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="fdb2f-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="fdb2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdb2f-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb2f-103">Ändert die Konfiguration eines Automatisierungszertifikats.</span><span class="sxs-lookup"><span data-stu-id="fdb2f-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="fdb2f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdb2f-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdb2f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fdb2f-105">DESCRIPTION</span></span>
<span data-ttu-id="fdb2f-106">Das **Cmdlet Set-AzAutomationCertificate** ändert die Konfiguration eines Zertifikats in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="fdb2f-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="fdb2f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fdb2f-107">EXAMPLES</span></span>

### <span data-ttu-id="fdb2f-108">Beispiel 1: Ändern eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="fdb2f-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fdb2f-109">Mit dem ersten Befehl wird ein Nur-Text-Kennwort mithilfe des cmdlets ConvertTo-SecureString in eine sichere Zeichenfolge konvertiert.</span><span class="sxs-lookup"><span data-stu-id="fdb2f-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="fdb2f-110">Der Befehl speichert dieses Objekt in der $Password Variablen.</span><span class="sxs-lookup"><span data-stu-id="fdb2f-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="fdb2f-111">Mit dem zweiten Befehl wird ein Zertifikat namens ContosoCertificate geändert.</span><span class="sxs-lookup"><span data-stu-id="fdb2f-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="fdb2f-112">Der Befehl verwendet das kennwort, das in $Password.</span><span class="sxs-lookup"><span data-stu-id="fdb2f-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="fdb2f-113">Der Befehl gibt den Kontonamen und den Pfad der Datei an, die hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="fdb2f-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="fdb2f-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fdb2f-114">PARAMETERS</span></span>

### <span data-ttu-id="fdb2f-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fdb2f-115">-AutomationAccountName</span></span>
<span data-ttu-id="fdb2f-116">Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet ein Zertifikat ändert.</span><span class="sxs-lookup"><span data-stu-id="fdb2f-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="fdb2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb2f-117">-DefaultProfile</span></span>
<span data-ttu-id="fdb2f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fdb2f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdb2f-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fdb2f-119">-Description</span></span>
<span data-ttu-id="fdb2f-120">Gibt eine Beschreibung für das Zertifikat an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="fdb2f-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fdb2f-121">-Exportierbar</span><span class="sxs-lookup"><span data-stu-id="fdb2f-121">-Exportable</span></span>
<span data-ttu-id="fdb2f-122">Gibt an, ob das Zertifikat exportiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fdb2f-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="fdb2f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="fdb2f-123">-Name</span></span>
<span data-ttu-id="fdb2f-124">Gibt den Namen des Zertifikats an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="fdb2f-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fdb2f-125">-Password</span><span class="sxs-lookup"><span data-stu-id="fdb2f-125">-Password</span></span>
<span data-ttu-id="fdb2f-126">Gibt das Kennwort für die Zertifikatdatei an.</span><span class="sxs-lookup"><span data-stu-id="fdb2f-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="fdb2f-127">-Path</span><span class="sxs-lookup"><span data-stu-id="fdb2f-127">-Path</span></span>
<span data-ttu-id="fdb2f-128">Gibt den Pfad zu einer Skriptdatei an, die hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fdb2f-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="fdb2f-129">Die Datei kann eine CER-Datei oder eine PFX-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="fdb2f-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="fdb2f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdb2f-130">-ResourceGroupName</span></span>
<span data-ttu-id="fdb2f-131">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet ein Zertifikat ändert.</span><span class="sxs-lookup"><span data-stu-id="fdb2f-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="fdb2f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb2f-132">CommonParameters</span></span>
<span data-ttu-id="fdb2f-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdb2f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb2f-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdb2f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb2f-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fdb2f-135">INPUTS</span></span>

### <span data-ttu-id="fdb2f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fdb2f-136">System.String</span></span>

### <span data-ttu-id="fdb2f-137">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="fdb2f-137">System.Security.SecureString</span></span>

### <span data-ttu-id="fdb2f-138">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fdb2f-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fdb2f-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fdb2f-139">OUTPUTS</span></span>

### <span data-ttu-id="fdb2f-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="fdb2f-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="fdb2f-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fdb2f-141">NOTES</span></span>

## <span data-ttu-id="fdb2f-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fdb2f-142">RELATED LINKS</span></span>

[<span data-ttu-id="fdb2f-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="fdb2f-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="fdb2f-144">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="fdb2f-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="fdb2f-145">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="fdb2f-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


