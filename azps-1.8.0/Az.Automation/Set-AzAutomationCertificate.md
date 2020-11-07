---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: f300f00558953db00bf99115a9d844b788d1f14a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661716"
---
# <span data-ttu-id="a1182-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a1182-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="a1182-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a1182-102">SYNOPSIS</span></span>
<span data-ttu-id="a1182-103">Ändert die Konfiguration eines Automatisierungs Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="a1182-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="a1182-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1182-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1182-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1182-105">DESCRIPTION</span></span>
<span data-ttu-id="a1182-106">Das Cmdlet " **Satz-AzAutomationCertificate** " ändert die Konfiguration eines Zertifikats in Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="a1182-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="a1182-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1182-107">EXAMPLES</span></span>

### <span data-ttu-id="a1182-108">Beispiel 1: Ändern eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="a1182-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a1182-109">Mit dem ersten Befehl wird ein nur-Text-Kennwort als sichere Zeichenfolge mithilfe des ConvertTo-SecureString-Cmdlets konvertiert.</span><span class="sxs-lookup"><span data-stu-id="a1182-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="a1182-110">Der Befehl speichert das Objekt in der $Password Variablen.</span><span class="sxs-lookup"><span data-stu-id="a1182-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="a1182-111">Der zweite Befehl ändert ein Zertifikat mit dem Namen ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="a1182-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="a1182-112">Der Befehl verwendet das in $Password gespeicherte Kennwort.</span><span class="sxs-lookup"><span data-stu-id="a1182-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="a1182-113">Der Befehl gibt den Kontonamen und den Pfad der Datei an, die er hochlädt.</span><span class="sxs-lookup"><span data-stu-id="a1182-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="a1182-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1182-114">PARAMETERS</span></span>

### <span data-ttu-id="a1182-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a1182-115">-AutomationAccountName</span></span>
<span data-ttu-id="a1182-116">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet ein Zertifikat geändert hat.</span><span class="sxs-lookup"><span data-stu-id="a1182-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="a1182-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1182-117">-DefaultProfile</span></span>
<span data-ttu-id="a1182-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a1182-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1182-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1182-119">-Description</span></span>
<span data-ttu-id="a1182-120">Gibt eine Beschreibung für das Zertifikat an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a1182-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a1182-121">-Exportierbar</span><span class="sxs-lookup"><span data-stu-id="a1182-121">-Exportable</span></span>
<span data-ttu-id="a1182-122">Gibt an, ob das Zertifikat exportiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a1182-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="a1182-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a1182-123">-Name</span></span>
<span data-ttu-id="a1182-124">Gibt den Namen des Zertifikats an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a1182-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a1182-125">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="a1182-125">-Password</span></span>
<span data-ttu-id="a1182-126">Gibt das Kennwort für die Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="a1182-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="a1182-127">-Path</span><span class="sxs-lookup"><span data-stu-id="a1182-127">-Path</span></span>
<span data-ttu-id="a1182-128">Gibt den Pfad zu einer Skriptdatei an, die hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1182-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="a1182-129">Die Datei kann eine CER-Datei oder eine PFX-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="a1182-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="a1182-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1182-130">-ResourceGroupName</span></span>
<span data-ttu-id="a1182-131">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet ein Zertifikat geändert hat.</span><span class="sxs-lookup"><span data-stu-id="a1182-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="a1182-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1182-132">CommonParameters</span></span>
<span data-ttu-id="a1182-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1182-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1182-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1182-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1182-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a1182-135">INPUTS</span></span>

### <span data-ttu-id="a1182-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a1182-136">System.String</span></span>

### <span data-ttu-id="a1182-137">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="a1182-137">System.Security.SecureString</span></span>

### <span data-ttu-id="a1182-138">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a1182-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a1182-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a1182-139">OUTPUTS</span></span>

### <span data-ttu-id="a1182-140">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="a1182-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="a1182-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="a1182-141">NOTES</span></span>

## <span data-ttu-id="a1182-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a1182-142">RELATED LINKS</span></span>

[<span data-ttu-id="a1182-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a1182-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="a1182-144">Neu – AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a1182-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="a1182-145">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a1182-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


