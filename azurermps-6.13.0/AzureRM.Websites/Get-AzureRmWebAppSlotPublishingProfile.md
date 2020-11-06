---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: 29ef83bf3ed0f423686e7ddf84bc82555bd09572
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93475862"
---
# <span data-ttu-id="3fd4c-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="3fd4c-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="3fd4c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3fd4c-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd4c-103">Ruft ein Azure Web App-Slot-Veröffentlichungsprofil ab.</span><span class="sxs-lookup"><span data-stu-id="3fd4c-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fd4c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fd4c-104">SYNTAX</span></span>

### <span data-ttu-id="3fd4c-105">S1</span><span class="sxs-lookup"><span data-stu-id="3fd4c-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3fd4c-106">S2</span><span class="sxs-lookup"><span data-stu-id="3fd4c-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3fd4c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3fd4c-107">DESCRIPTION</span></span>
<span data-ttu-id="3fd4c-108">Das Cmdlet " **Get-AzureRmWebAppSlotPublishingProfile** " Ruft das Web App-Veröffentlichungsprofil für den angegebenen Slot ab.</span><span class="sxs-lookup"><span data-stu-id="3fd4c-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="3fd4c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3fd4c-109">EXAMPLES</span></span>

### <span data-ttu-id="3fd4c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3fd4c-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="3fd4c-111">Dieser Befehl ruft das Veröffentlichungsprofil im FTP-Format für Slot Slot001 in Bezug auf das Web-App-ContosoWebApp ab, das der Ressourcengruppe Default-Web-westus zugeordnet ist, und speichert Sie in der angegebenen Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="3fd4c-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="3fd4c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fd4c-112">PARAMETERS</span></span>

### <span data-ttu-id="3fd4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fd4c-113">-DefaultProfile</span></span>
<span data-ttu-id="3fd4c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3fd4c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd4c-115">-Format</span><span class="sxs-lookup"><span data-stu-id="3fd4c-115">-Format</span></span>
<span data-ttu-id="3fd4c-116">Format</span><span class="sxs-lookup"><span data-stu-id="3fd4c-116">Format</span></span>

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

### <span data-ttu-id="3fd4c-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="3fd4c-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="3fd4c-118">Einbeziehen der Disaster Recovery-Endpunkte bei true</span><span class="sxs-lookup"><span data-stu-id="3fd4c-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd4c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3fd4c-119">-Name</span></span>
<span data-ttu-id="3fd4c-120">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="3fd4c-120">WebApp Name</span></span>

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

### <span data-ttu-id="3fd4c-121">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="3fd4c-121">-OutputFile</span></span>
<span data-ttu-id="3fd4c-122">Ausgabedatei</span><span class="sxs-lookup"><span data-stu-id="3fd4c-122">Output File</span></span>

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

### <span data-ttu-id="3fd4c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fd4c-123">-ResourceGroupName</span></span>
<span data-ttu-id="3fd4c-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="3fd4c-124">Resource Group Name</span></span>

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

### <span data-ttu-id="3fd4c-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="3fd4c-125">-Slot</span></span>
<span data-ttu-id="3fd4c-126">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="3fd4c-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="3fd4c-127">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="3fd4c-127">-WebApp</span></span>
<span data-ttu-id="3fd4c-128">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="3fd4c-128">WebApp Object</span></span>

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

### <span data-ttu-id="3fd4c-129">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="3fd4c-129">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="3fd4c-130">Einbeziehen der Disaster Recovery-Endpunkte bei true</span><span class="sxs-lookup"><span data-stu-id="3fd4c-130">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd4c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd4c-131">CommonParameters</span></span>
<span data-ttu-id="3fd4c-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fd4c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fd4c-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fd4c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd4c-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3fd4c-134">INPUTS</span></span>

### <span data-ttu-id="3fd4c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3fd4c-135">System.String</span></span>

### <span data-ttu-id="3fd4c-136">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="3fd4c-136">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="3fd4c-137">Parameter: webByValue</span><span class="sxs-lookup"><span data-stu-id="3fd4c-137">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="3fd4c-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3fd4c-138">OUTPUTS</span></span>

### <span data-ttu-id="3fd4c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3fd4c-139">System.String</span></span>

## <span data-ttu-id="3fd4c-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="3fd4c-140">NOTES</span></span>

## <span data-ttu-id="3fd4c-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3fd4c-141">RELATED LINKS</span></span>

[<span data-ttu-id="3fd4c-142">Reset-AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="3fd4c-142">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="3fd4c-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3fd4c-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="3fd4c-144">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3fd4c-144">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
