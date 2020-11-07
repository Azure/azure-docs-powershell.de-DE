---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: a89ebd3142d738664cd80cab198bd6f791c1287a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658559"
---
# <span data-ttu-id="93915-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="93915-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="93915-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93915-102">SYNOPSIS</span></span>
<span data-ttu-id="93915-103">Ruft ein Azure Web App-Veröffentlichungsprofil ab.</span><span class="sxs-lookup"><span data-stu-id="93915-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="93915-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93915-104">SYNTAX</span></span>

### <span data-ttu-id="93915-105">S1</span><span class="sxs-lookup"><span data-stu-id="93915-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93915-106">S2</span><span class="sxs-lookup"><span data-stu-id="93915-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93915-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93915-107">DESCRIPTION</span></span>
<span data-ttu-id="93915-108">Das Cmdlet " **Get-AzWebAppPublishingProfile** " Ruft ein Azure Web App-Veröffentlichungsprofil ab.</span><span class="sxs-lookup"><span data-stu-id="93915-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="93915-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93915-109">EXAMPLES</span></span>

### <span data-ttu-id="93915-110">1:</span><span class="sxs-lookup"><span data-stu-id="93915-110">1:</span></span>
```
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="93915-111">Dieser Befehl ruft das Veröffentlichungsprofil im FTP-Format für Web App-ContosoWebApp ab, das der Ressourcengruppe Default-Web-westus zugeordnet ist, und speichert Sie in der angegebenen Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="93915-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="93915-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="93915-112">PARAMETERS</span></span>

### <span data-ttu-id="93915-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93915-113">-DefaultProfile</span></span>
<span data-ttu-id="93915-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93915-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93915-115">-Format</span><span class="sxs-lookup"><span data-stu-id="93915-115">-Format</span></span>
<span data-ttu-id="93915-116">Format</span><span class="sxs-lookup"><span data-stu-id="93915-116">Format</span></span>

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

### <span data-ttu-id="93915-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="93915-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="93915-118">Einbeziehen der Disaster Recovery-Endpunkte bei true</span><span class="sxs-lookup"><span data-stu-id="93915-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="93915-119">-Name</span><span class="sxs-lookup"><span data-stu-id="93915-119">-Name</span></span>
<span data-ttu-id="93915-120">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="93915-120">WebApp Name</span></span>

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

### <span data-ttu-id="93915-121">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="93915-121">-OutputFile</span></span>
<span data-ttu-id="93915-122">Ausgabedatei</span><span class="sxs-lookup"><span data-stu-id="93915-122">Output File</span></span>

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

### <span data-ttu-id="93915-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93915-123">-ResourceGroupName</span></span>
<span data-ttu-id="93915-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="93915-124">Resource Group Name</span></span>

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

### <span data-ttu-id="93915-125">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="93915-125">-WebApp</span></span>
<span data-ttu-id="93915-126">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="93915-126">WebApp Object</span></span>

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

### <span data-ttu-id="93915-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93915-127">CommonParameters</span></span>
<span data-ttu-id="93915-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93915-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93915-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93915-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93915-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93915-130">INPUTS</span></span>

### <span data-ttu-id="93915-131">System. String</span><span class="sxs-lookup"><span data-stu-id="93915-131">System.String</span></span>

### <span data-ttu-id="93915-132">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="93915-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="93915-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93915-133">OUTPUTS</span></span>

### <span data-ttu-id="93915-134">System. String</span><span class="sxs-lookup"><span data-stu-id="93915-134">System.String</span></span>

## <span data-ttu-id="93915-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="93915-135">NOTES</span></span>

## <span data-ttu-id="93915-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93915-136">RELATED LINKS</span></span>

[<span data-ttu-id="93915-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="93915-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="93915-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="93915-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


