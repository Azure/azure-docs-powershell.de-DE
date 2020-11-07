---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 615fcc228be9ef0e3e0d23c6463859c20ff7da11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821183"
---
# <span data-ttu-id="b3da3-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="b3da3-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="b3da3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b3da3-102">SYNOPSIS</span></span>
<span data-ttu-id="b3da3-103">Ruft ein Azure Web App-Slot-Veröffentlichungsprofil ab.</span><span class="sxs-lookup"><span data-stu-id="b3da3-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="b3da3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3da3-104">SYNTAX</span></span>

### <span data-ttu-id="b3da3-105">S1</span><span class="sxs-lookup"><span data-stu-id="b3da3-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3da3-106">S2</span><span class="sxs-lookup"><span data-stu-id="b3da3-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3da3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3da3-107">DESCRIPTION</span></span>
<span data-ttu-id="b3da3-108">Das Cmdlet " **Get-AzWebAppSlotPublishingProfile** " Ruft das Web App-Veröffentlichungsprofil für den angegebenen Slot ab.</span><span class="sxs-lookup"><span data-stu-id="b3da3-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="b3da3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3da3-109">EXAMPLES</span></span>

### <span data-ttu-id="b3da3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b3da3-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="b3da3-111">Dieser Befehl ruft das Veröffentlichungsprofil im FTP-Format für Slot Slot001 in Bezug auf das Web-App-ContosoWebApp ab, das der Ressourcengruppe Default-Web-westus zugeordnet ist, und speichert Sie in der angegebenen Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="b3da3-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="b3da3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3da3-112">PARAMETERS</span></span>

### <span data-ttu-id="b3da3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3da3-113">-DefaultProfile</span></span>
<span data-ttu-id="b3da3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b3da3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3da3-115">-Format</span><span class="sxs-lookup"><span data-stu-id="b3da3-115">-Format</span></span>
<span data-ttu-id="b3da3-116">Format</span><span class="sxs-lookup"><span data-stu-id="b3da3-116">Format</span></span>

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

### <span data-ttu-id="b3da3-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="b3da3-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="b3da3-118">Einbeziehen der Disaster Recovery-Endpunkte bei true</span><span class="sxs-lookup"><span data-stu-id="b3da3-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="b3da3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b3da3-119">-Name</span></span>
<span data-ttu-id="b3da3-120">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="b3da3-120">WebApp Name</span></span>

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

### <span data-ttu-id="b3da3-121">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="b3da3-121">-OutputFile</span></span>
<span data-ttu-id="b3da3-122">Ausgabedatei</span><span class="sxs-lookup"><span data-stu-id="b3da3-122">Output File</span></span>

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

### <span data-ttu-id="b3da3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3da3-123">-ResourceGroupName</span></span>
<span data-ttu-id="b3da3-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="b3da3-124">Resource Group Name</span></span>

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

### <span data-ttu-id="b3da3-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="b3da3-125">-Slot</span></span>
<span data-ttu-id="b3da3-126">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="b3da3-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="b3da3-127">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="b3da3-127">-WebApp</span></span>
<span data-ttu-id="b3da3-128">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="b3da3-128">WebApp Object</span></span>

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

### <span data-ttu-id="b3da3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3da3-129">CommonParameters</span></span>
<span data-ttu-id="b3da3-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3da3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3da3-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3da3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3da3-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b3da3-132">INPUTS</span></span>

### <span data-ttu-id="b3da3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b3da3-133">System.String</span></span>

### <span data-ttu-id="b3da3-134">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="b3da3-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b3da3-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b3da3-135">OUTPUTS</span></span>

### <span data-ttu-id="b3da3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b3da3-136">System.String</span></span>

## <span data-ttu-id="b3da3-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="b3da3-137">NOTES</span></span>

## <span data-ttu-id="b3da3-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b3da3-138">RELATED LINKS</span></span>

[<span data-ttu-id="b3da3-139">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="b3da3-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="b3da3-140">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b3da3-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="b3da3-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b3da3-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
