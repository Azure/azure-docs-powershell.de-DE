---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3422EFD0-88DC-4DF0-868C-5C63C9FA95EF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9aa78f34abf17c2aa5858697f492f76ee124d91
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005896"
---
# <span data-ttu-id="8637b-101">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8637b-101">Disable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="8637b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8637b-102">SYNOPSIS</span></span>
<span data-ttu-id="8637b-103">Deaktiviert die Anwendungs Diagnose für eine Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="8637b-103">Disables application diagnostics for an Azure website.</span></span>

## <span data-ttu-id="8637b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8637b-104">SYNTAX</span></span>

```
Disable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] [-TableStorage] [-BlobStorage] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8637b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8637b-105">DESCRIPTION</span></span>
<span data-ttu-id="8637b-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8637b-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8637b-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8637b-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8637b-108">Deaktiviert die Anwendungs Diagnose für eine Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="8637b-108">Disables application diagnostics for an Azure website.</span></span>
<span data-ttu-id="8637b-109">Deaktiviert die Protokollierung, die für die Speicherung in einem Dateisystem oder auf Azure konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="8637b-109">Disables logging configured to be stored on a file system or on Azure.</span></span>

## <span data-ttu-id="8637b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8637b-110">EXAMPLES</span></span>

### <span data-ttu-id="8637b-111">Beispiel 1: Deaktivieren der Anwendungs Protokollierungsdatei</span><span class="sxs-lookup"><span data-stu-id="8637b-111">Example 1:  Disable application logging file</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File
```

<span data-ttu-id="8637b-112">Im folgenden Beispiel wird die Anwendungsprotokollierung für das Dateisystem deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8637b-112">The following example disables application logging on the file system.</span></span>

### <span data-ttu-id="8637b-113">Beispiel 2: Deaktivieren der Protokollierung mithilfe des Azure-Speichers</span><span class="sxs-lookup"><span data-stu-id="8637b-113">Example 2:  Disable logging using Azure storage</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage
```

<span data-ttu-id="8637b-114">Im folgenden Beispiel wird die Anwendungsprotokollierung mithilfe von Speicher deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8637b-114">The following example disables application logging using storage.</span></span>

## <span data-ttu-id="8637b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="8637b-115">PARAMETERS</span></span>

### <span data-ttu-id="8637b-116">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="8637b-116">-BlobStorage</span></span>
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

### <span data-ttu-id="8637b-117">-Datei</span><span class="sxs-lookup"><span data-stu-id="8637b-117">-File</span></span>
<span data-ttu-id="8637b-118">Gibt an, dass Sie das Dateisystem zum Speichern der Protokolldateien verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="8637b-118">Specifies that you want to use the file system to store the log files.</span></span>

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

### <span data-ttu-id="8637b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8637b-119">-Name</span></span>
<span data-ttu-id="8637b-120">Gibt den Namen der Website an.</span><span class="sxs-lookup"><span data-stu-id="8637b-120">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="8637b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8637b-121">-PassThru</span></span>
<span data-ttu-id="8637b-122">Flag, um true zurückzugeben, wenn dies erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="8637b-122">Flag to return true if succeeded.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8637b-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="8637b-123">-Profile</span></span>
<span data-ttu-id="8637b-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8637b-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8637b-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8637b-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8637b-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="8637b-126">-Slot</span></span>
<span data-ttu-id="8637b-127">Gibt den Namen des Steckplatzes an.</span><span class="sxs-lookup"><span data-stu-id="8637b-127">Specifies the name of slot.</span></span>

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

### <span data-ttu-id="8637b-128">-Speicher</span><span class="sxs-lookup"><span data-stu-id="8637b-128">-TableStorage</span></span>
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

### <span data-ttu-id="8637b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8637b-129">CommonParameters</span></span>
<span data-ttu-id="8637b-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8637b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8637b-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8637b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8637b-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8637b-132">INPUTS</span></span>

## <span data-ttu-id="8637b-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8637b-133">OUTPUTS</span></span>

## <span data-ttu-id="8637b-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="8637b-134">NOTES</span></span>

## <span data-ttu-id="8637b-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8637b-135">RELATED LINKS</span></span>

[<span data-ttu-id="8637b-136">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8637b-136">Enable-AzureWebsiteApplicationDiagnostic</span></span>](./Enable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="8637b-137">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8637b-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="8637b-138">Neu – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8637b-138">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="8637b-139">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8637b-139">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="8637b-140">Anfang-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8637b-140">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


