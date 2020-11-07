---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 56b3c942fe033f32b18c19ec669b19d87397c5bc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845743"
---
# <span data-ttu-id="126c4-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="126c4-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="126c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="126c4-102">SYNOPSIS</span></span>
<span data-ttu-id="126c4-103">Ruft ein Azure Web App-Veröffentlichungsprofil ab.</span><span class="sxs-lookup"><span data-stu-id="126c4-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="126c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="126c4-104">SYNTAX</span></span>

### <span data-ttu-id="126c4-105">S1</span><span class="sxs-lookup"><span data-stu-id="126c4-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="126c4-106">S2</span><span class="sxs-lookup"><span data-stu-id="126c4-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="126c4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="126c4-107">DESCRIPTION</span></span>
<span data-ttu-id="126c4-108">Das Cmdlet " **Get-AzWebAppPublishingProfile** " Ruft ein Azure Web App-Veröffentlichungsprofil ab.</span><span class="sxs-lookup"><span data-stu-id="126c4-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="126c4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="126c4-109">EXAMPLES</span></span>

### <span data-ttu-id="126c4-110">1:</span><span class="sxs-lookup"><span data-stu-id="126c4-110">1:</span></span>
```
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile.publishsettings"
```

<span data-ttu-id="126c4-111">Dieser Befehl ruft das Veröffentlichungsprofil im FTP-Format für Web App-ContosoWebApp ab, das der Ressourcengruppe Default-Web-westus zugeordnet ist, und speichert Sie in der angegebenen Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="126c4-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="126c4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="126c4-112">PARAMETERS</span></span>

### <span data-ttu-id="126c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="126c4-113">-DefaultProfile</span></span>
<span data-ttu-id="126c4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="126c4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="126c4-115">-Format</span><span class="sxs-lookup"><span data-stu-id="126c4-115">-Format</span></span>
<span data-ttu-id="126c4-116">Format</span><span class="sxs-lookup"><span data-stu-id="126c4-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="126c4-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="126c4-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="126c4-118">Einbeziehen der Disaster Recovery-Endpunkte bei true</span><span class="sxs-lookup"><span data-stu-id="126c4-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="126c4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="126c4-119">-Name</span></span>
<span data-ttu-id="126c4-120">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="126c4-120">WebApp Name</span></span>

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

### <span data-ttu-id="126c4-121">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="126c4-121">-OutputFile</span></span>
<span data-ttu-id="126c4-122">Ausgabedatei</span><span class="sxs-lookup"><span data-stu-id="126c4-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="126c4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="126c4-123">-ResourceGroupName</span></span>
<span data-ttu-id="126c4-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="126c4-124">Resource Group Name</span></span>

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

### <span data-ttu-id="126c4-125">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="126c4-125">-WebApp</span></span>
<span data-ttu-id="126c4-126">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="126c4-126">WebApp Object</span></span>

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

### <span data-ttu-id="126c4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="126c4-127">CommonParameters</span></span>
<span data-ttu-id="126c4-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="126c4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="126c4-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="126c4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="126c4-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="126c4-130">INPUTS</span></span>

### <span data-ttu-id="126c4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="126c4-131">System.String</span></span>

### <span data-ttu-id="126c4-132">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="126c4-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="126c4-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="126c4-133">OUTPUTS</span></span>

### <span data-ttu-id="126c4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="126c4-134">System.String</span></span>

## <span data-ttu-id="126c4-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="126c4-135">NOTES</span></span>

## <span data-ttu-id="126c4-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="126c4-136">RELATED LINKS</span></span>

[<span data-ttu-id="126c4-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="126c4-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="126c4-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="126c4-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


