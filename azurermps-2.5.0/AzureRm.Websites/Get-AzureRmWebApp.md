---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: eb1f96eaf85e6a5e7234e09c319b2e0c1117d456
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848059"
---
# <span data-ttu-id="f7c1a-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f7c1a-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="f7c1a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="f7c1a-103">Ruft Azure Web Apps in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="f7c1a-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7c1a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7c1a-104">SYNTAX</span></span>

### <span data-ttu-id="f7c1a-105">S1</span><span class="sxs-lookup"><span data-stu-id="f7c1a-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7c1a-106">S2</span><span class="sxs-lookup"><span data-stu-id="f7c1a-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <AppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7c1a-107">S3</span><span class="sxs-lookup"><span data-stu-id="f7c1a-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7c1a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7c1a-108">DESCRIPTION</span></span>
<span data-ttu-id="f7c1a-109">Das Cmdlet " **Get-AzureRmWebApp** " Ruft Informationen zu einer Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="f7c1a-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="f7c1a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7c1a-110">EXAMPLES</span></span>

### <span data-ttu-id="f7c1a-111">Beispiel 1: Abrufen einer Web-App aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f7c1a-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="f7c1a-112">Dieser Befehl ruft die Web-App mit dem Namen ContosoSite ab, die der Ressourcengruppe Default-Web-westus angehört.</span><span class="sxs-lookup"><span data-stu-id="f7c1a-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f7c1a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7c1a-113">PARAMETERS</span></span>

### <span data-ttu-id="f7c1a-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f7c1a-114">-AppServicePlan</span></span>
<span data-ttu-id="f7c1a-115">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="f7c1a-115">App Service Plan object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c1a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7c1a-116">-DefaultProfile</span></span>
<span data-ttu-id="f7c1a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f7c1a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7c1a-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="f7c1a-118">-Location</span></span>
<span data-ttu-id="f7c1a-119">Lage</span><span class="sxs-lookup"><span data-stu-id="f7c1a-119">Location</span></span>

```yaml
Type: String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c1a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f7c1a-120">-Name</span></span>
<span data-ttu-id="f7c1a-121">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="f7c1a-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7c1a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7c1a-122">-ResourceGroupName</span></span>
<span data-ttu-id="f7c1a-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="f7c1a-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7c1a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7c1a-124">CommonParameters</span></span>
<span data-ttu-id="f7c1a-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7c1a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7c1a-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7c1a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7c1a-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7c1a-127">INPUTS</span></span>

### <span data-ttu-id="f7c1a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f7c1a-128">System.String</span></span>

## <span data-ttu-id="f7c1a-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7c1a-129">OUTPUTS</span></span>

### <span data-ttu-id="f7c1a-130">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="f7c1a-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="f7c1a-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7c1a-131">NOTES</span></span>

## <span data-ttu-id="f7c1a-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7c1a-132">RELATED LINKS</span></span>

[<span data-ttu-id="f7c1a-133">Neu – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f7c1a-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="f7c1a-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f7c1a-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="f7c1a-135">Neustart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f7c1a-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="f7c1a-136">Anfang-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f7c1a-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="f7c1a-137">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f7c1a-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


