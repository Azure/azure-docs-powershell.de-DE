---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
ms.openlocfilehash: 64945cf503248fc0561dc894090c73d2d7151e4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663282"
---
# <span data-ttu-id="0fbf6-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0fbf6-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="0fbf6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0fbf6-102">SYNOPSIS</span></span>
<span data-ttu-id="0fbf6-103">Ruft Azure Web Apps in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="0fbf6-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fbf6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fbf6-104">SYNTAX</span></span>

### <span data-ttu-id="0fbf6-105">S1</span><span class="sxs-lookup"><span data-stu-id="0fbf6-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0fbf6-106">S2</span><span class="sxs-lookup"><span data-stu-id="0fbf6-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0fbf6-107">S3</span><span class="sxs-lookup"><span data-stu-id="0fbf6-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fbf6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fbf6-108">DESCRIPTION</span></span>
<span data-ttu-id="0fbf6-109">Das Cmdlet " **Get-AzureRmWebApp** " Ruft Informationen zu einer Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="0fbf6-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="0fbf6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0fbf6-110">EXAMPLES</span></span>

### <span data-ttu-id="0fbf6-111">Beispiel 1: Abrufen einer Web-App aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0fbf6-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -SlotName "Slot001"
```

<span data-ttu-id="0fbf6-112">Dieser Befehl ruft die Web-App mit dem Namen ContosoSite ab, die der Ressourcengruppe Default-Web-westus angehört.</span><span class="sxs-lookup"><span data-stu-id="0fbf6-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="0fbf6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fbf6-113">PARAMETERS</span></span>

### <span data-ttu-id="0fbf6-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0fbf6-114">-AppServicePlan</span></span>
<span data-ttu-id="0fbf6-115">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="0fbf6-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fbf6-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="0fbf6-116">-Location</span></span>
<span data-ttu-id="0fbf6-117">Lage</span><span class="sxs-lookup"><span data-stu-id="0fbf6-117">Location</span></span>

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

### <span data-ttu-id="0fbf6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0fbf6-118">-Name</span></span>
<span data-ttu-id="0fbf6-119">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="0fbf6-119">WebApp Name</span></span>

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

### <span data-ttu-id="0fbf6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fbf6-120">-ResourceGroupName</span></span>
<span data-ttu-id="0fbf6-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="0fbf6-121">Resource Group Name</span></span>

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

### <span data-ttu-id="0fbf6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fbf6-122">-DefaultProfile</span></span>
<span data-ttu-id="0fbf6-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0fbf6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fbf6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fbf6-124">CommonParameters</span></span>
<span data-ttu-id="0fbf6-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fbf6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fbf6-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fbf6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fbf6-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0fbf6-127">INPUTS</span></span>

## <span data-ttu-id="0fbf6-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0fbf6-128">OUTPUTS</span></span>

## <span data-ttu-id="0fbf6-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="0fbf6-129">NOTES</span></span>

## <span data-ttu-id="0fbf6-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0fbf6-130">RELATED LINKS</span></span>

[<span data-ttu-id="0fbf6-131">Neu – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0fbf6-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="0fbf6-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0fbf6-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="0fbf6-133">Neustart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0fbf6-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="0fbf6-134">Anfang-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0fbf6-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="0fbf6-135">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0fbf6-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


