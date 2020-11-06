---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
ms.openlocfilehash: 83afdb179a9c0f135fd17827ff59f89ad117e3b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497181"
---
# <span data-ttu-id="7f90b-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7f90b-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="7f90b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f90b-102">SYNOPSIS</span></span>
<span data-ttu-id="7f90b-103">Ruft Azure Web Apps in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="7f90b-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f90b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f90b-104">SYNTAX</span></span>

### <span data-ttu-id="7f90b-105">S1</span><span class="sxs-lookup"><span data-stu-id="7f90b-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f90b-106">S2</span><span class="sxs-lookup"><span data-stu-id="7f90b-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f90b-107">S3</span><span class="sxs-lookup"><span data-stu-id="7f90b-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f90b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f90b-108">DESCRIPTION</span></span>
<span data-ttu-id="7f90b-109">Das Cmdlet " **Get-AzureRmWebApp** " Ruft Informationen zu einer Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="7f90b-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="7f90b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f90b-110">EXAMPLES</span></span>

### <span data-ttu-id="7f90b-111">Beispiel 1: Abrufen einer Web-App aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7f90b-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="7f90b-112">Dieser Befehl ruft die Web-App mit dem Namen ContosoSite ab, die der Ressourcengruppe Default-Web-westus angehört.</span><span class="sxs-lookup"><span data-stu-id="7f90b-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="7f90b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f90b-113">PARAMETERS</span></span>

### <span data-ttu-id="7f90b-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7f90b-114">-AppServicePlan</span></span>
<span data-ttu-id="7f90b-115">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="7f90b-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f90b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f90b-116">-DefaultProfile</span></span>
<span data-ttu-id="7f90b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f90b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f90b-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="7f90b-118">-Location</span></span>
<span data-ttu-id="7f90b-119">Lage</span><span class="sxs-lookup"><span data-stu-id="7f90b-119">Location</span></span>

```yaml
Type: System.String
Parameter Sets: S3
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f90b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7f90b-120">-Name</span></span>
<span data-ttu-id="7f90b-121">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="7f90b-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f90b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f90b-122">-ResourceGroupName</span></span>
<span data-ttu-id="7f90b-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="7f90b-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f90b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f90b-124">CommonParameters</span></span>
<span data-ttu-id="7f90b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f90b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f90b-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f90b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f90b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f90b-127">INPUTS</span></span>

### <span data-ttu-id="7f90b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7f90b-128">System.String</span></span>

## <span data-ttu-id="7f90b-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f90b-129">OUTPUTS</span></span>

### <span data-ttu-id="7f90b-130">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="7f90b-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="7f90b-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f90b-131">NOTES</span></span>

## <span data-ttu-id="7f90b-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f90b-132">RELATED LINKS</span></span>

[<span data-ttu-id="7f90b-133">Neu – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7f90b-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="7f90b-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7f90b-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="7f90b-135">Neustart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7f90b-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="7f90b-136">Anfang-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7f90b-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="7f90b-137">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7f90b-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


