---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: fed1be90af7aad2126b20dbe830f5069cc62e01f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940680"
---
# <span data-ttu-id="549f1-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="549f1-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="549f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="549f1-102">SYNOPSIS</span></span>
<span data-ttu-id="549f1-103">Ruft ein Azure Web App-Slotveröffentlichungsprofil ab.</span><span class="sxs-lookup"><span data-stu-id="549f1-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="549f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="549f1-104">SYNTAX</span></span>

### <span data-ttu-id="549f1-105">S1</span><span class="sxs-lookup"><span data-stu-id="549f1-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="549f1-106">S2</span><span class="sxs-lookup"><span data-stu-id="549f1-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="549f1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="549f1-107">DESCRIPTION</span></span>
<span data-ttu-id="549f1-108">Das **Get-AzWebAppSlotPublishingProfile-Cmdlet** ruft das Web App-Veröffentlichungsprofil für den angegebenen Slot ab.</span><span class="sxs-lookup"><span data-stu-id="549f1-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="549f1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="549f1-109">EXAMPLES</span></span>

### <span data-ttu-id="549f1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="549f1-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="549f1-111">Dieser Befehl ruft das Veröffentlichungsprofil im Ftp-Format für Slot Slot001 ab, das sich auf die Web App ContosoWebApp bezieht, die der Ressourcengruppe Default-Web-WestUS zugeordnet ist, und speichert es in der angegebenen Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="549f1-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="549f1-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="549f1-112">PARAMETERS</span></span>

### <span data-ttu-id="549f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="549f1-113">-DefaultProfile</span></span>
<span data-ttu-id="549f1-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="549f1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="549f1-115">-Format</span><span class="sxs-lookup"><span data-stu-id="549f1-115">-Format</span></span>
<span data-ttu-id="549f1-116">Format</span><span class="sxs-lookup"><span data-stu-id="549f1-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="549f1-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="549f1-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="549f1-118">Schließen Sie die Endpunkte für die Notfallwiederherstellung ein, wenn wahr</span><span class="sxs-lookup"><span data-stu-id="549f1-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="549f1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="549f1-119">-Name</span></span>
<span data-ttu-id="549f1-120">WebApp-Name</span><span class="sxs-lookup"><span data-stu-id="549f1-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="549f1-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="549f1-121">-OutputFile</span></span>
<span data-ttu-id="549f1-122">Ausgabedatei</span><span class="sxs-lookup"><span data-stu-id="549f1-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="549f1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="549f1-123">-ResourceGroupName</span></span>
<span data-ttu-id="549f1-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="549f1-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="549f1-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="549f1-125">-Slot</span></span>
<span data-ttu-id="549f1-126">WebApp Slot Name</span><span class="sxs-lookup"><span data-stu-id="549f1-126">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="549f1-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="549f1-127">-WebApp</span></span>
<span data-ttu-id="549f1-128">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="549f1-128">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="549f1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="549f1-129">CommonParameters</span></span>
<span data-ttu-id="549f1-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="549f1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="549f1-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="549f1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="549f1-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="549f1-132">INPUTS</span></span>

### <span data-ttu-id="549f1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="549f1-133">System.String</span></span>

### <span data-ttu-id="549f1-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="549f1-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="549f1-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="549f1-135">OUTPUTS</span></span>

### <span data-ttu-id="549f1-136">System.String</span><span class="sxs-lookup"><span data-stu-id="549f1-136">System.String</span></span>

## <span data-ttu-id="549f1-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="549f1-137">NOTES</span></span>

## <span data-ttu-id="549f1-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="549f1-138">RELATED LINKS</span></span>

[<span data-ttu-id="549f1-139">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="549f1-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="549f1-140">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="549f1-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="549f1-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="549f1-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
