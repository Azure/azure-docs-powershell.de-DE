---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
ms.openlocfilehash: a1858419b20bf85a40f94e2b5016b461cd24c39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501558"
---
# <span data-ttu-id="eb714-101">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="eb714-101">Set-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="eb714-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb714-102">SYNOPSIS</span></span>
<span data-ttu-id="eb714-103">Ändert die Konfiguration eines Automatisierungs Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="eb714-103">Modifies the configuration of an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb714-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb714-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb714-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb714-105">DESCRIPTION</span></span>
<span data-ttu-id="eb714-106">Das Cmdlet " **Satz-AzureRmAutomationCertificate** " ändert die Konfiguration eines Zertifikats in Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="eb714-106">The **Set-AzureRmAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="eb714-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb714-107">EXAMPLES</span></span>

### <span data-ttu-id="eb714-108">Beispiel 1: Ändern eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="eb714-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="eb714-109">Mit dem ersten Befehl wird ein nur-Text-Kennwort als sichere Zeichenfolge mithilfe des ConvertTo-SecureString-Cmdlets konvertiert.</span><span class="sxs-lookup"><span data-stu-id="eb714-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="eb714-110">Der Befehl speichert das Objekt in der $Password Variablen.</span><span class="sxs-lookup"><span data-stu-id="eb714-110">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="eb714-111">Der zweite Befehl ändert ein Zertifikat mit dem Namen ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="eb714-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="eb714-112">Der Befehl verwendet das in $Password gespeicherte Kennwort.</span><span class="sxs-lookup"><span data-stu-id="eb714-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="eb714-113">Der Befehl gibt den Kontonamen und den Pfad der Datei an, die er hochlädt.</span><span class="sxs-lookup"><span data-stu-id="eb714-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="eb714-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb714-114">PARAMETERS</span></span>

### <span data-ttu-id="eb714-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="eb714-115">-AutomationAccountName</span></span>
<span data-ttu-id="eb714-116">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet ein Zertifikat geändert hat.</span><span class="sxs-lookup"><span data-stu-id="eb714-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb714-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb714-117">-DefaultProfile</span></span>
<span data-ttu-id="eb714-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="eb714-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb714-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb714-119">-Description</span></span>
<span data-ttu-id="eb714-120">Gibt eine Beschreibung für das Zertifikat an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="eb714-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="eb714-121">-Exportierbar</span><span class="sxs-lookup"><span data-stu-id="eb714-121">-Exportable</span></span>
<span data-ttu-id="eb714-122">Gibt an, ob das Zertifikat exportiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="eb714-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="eb714-123">-Name</span><span class="sxs-lookup"><span data-stu-id="eb714-123">-Name</span></span>
<span data-ttu-id="eb714-124">Gibt den Namen des Zertifikats an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="eb714-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb714-125">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="eb714-125">-Password</span></span>
<span data-ttu-id="eb714-126">Gibt das Kennwort für die Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="eb714-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="eb714-127">-Path</span><span class="sxs-lookup"><span data-stu-id="eb714-127">-Path</span></span>
<span data-ttu-id="eb714-128">Gibt den Pfad zu einer Skriptdatei an, die hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb714-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="eb714-129">Die Datei kann eine CER-Datei oder eine PFX-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="eb714-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="eb714-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb714-130">-ResourceGroupName</span></span>
<span data-ttu-id="eb714-131">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet ein Zertifikat geändert hat.</span><span class="sxs-lookup"><span data-stu-id="eb714-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb714-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb714-132">CommonParameters</span></span>
<span data-ttu-id="eb714-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb714-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb714-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb714-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb714-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb714-135">INPUTS</span></span>

### <span data-ttu-id="eb714-136">Keine</span><span class="sxs-lookup"><span data-stu-id="eb714-136">None</span></span>
<span data-ttu-id="eb714-137">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="eb714-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb714-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb714-138">OUTPUTS</span></span>

### <span data-ttu-id="eb714-139">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="eb714-139">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="eb714-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb714-140">NOTES</span></span>

## <span data-ttu-id="eb714-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb714-141">RELATED LINKS</span></span>

[<span data-ttu-id="eb714-142">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="eb714-142">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="eb714-143">Neu – AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="eb714-143">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="eb714-144">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="eb714-144">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)


