---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: d1217f3abc00fec8752fcddbb30e577df087b5de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821180"
---
# <span data-ttu-id="b6512-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b6512-101">Get-AzWebApp</span></span>

## <span data-ttu-id="b6512-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6512-102">SYNOPSIS</span></span>
<span data-ttu-id="b6512-103">Ruft Azure Web Apps in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="b6512-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="b6512-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6512-104">SYNTAX</span></span>

### <span data-ttu-id="b6512-105">S1</span><span class="sxs-lookup"><span data-stu-id="b6512-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6512-106">S2</span><span class="sxs-lookup"><span data-stu-id="b6512-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6512-107">S3</span><span class="sxs-lookup"><span data-stu-id="b6512-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6512-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6512-108">DESCRIPTION</span></span>
<span data-ttu-id="b6512-109">Das Cmdlet " **Get-AzWebApp** " Ruft Informationen zu einer Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="b6512-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="b6512-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6512-110">EXAMPLES</span></span>

### <span data-ttu-id="b6512-111">Beispiel 1: Abrufen einer Web-App aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b6512-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="b6512-112">Dieser Befehl ruft die Web-App mit dem Namen ContosoSite ab, die der Ressourcengruppe Default-Web-westus angehört.</span><span class="sxs-lookup"><span data-stu-id="b6512-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b6512-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6512-113">PARAMETERS</span></span>

### <span data-ttu-id="b6512-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b6512-114">-AppServicePlan</span></span>
<span data-ttu-id="b6512-115">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="b6512-115">App Service Plan object</span></span>

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

### <span data-ttu-id="b6512-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6512-116">-DefaultProfile</span></span>
<span data-ttu-id="b6512-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b6512-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6512-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="b6512-118">-Location</span></span>
<span data-ttu-id="b6512-119">Lage</span><span class="sxs-lookup"><span data-stu-id="b6512-119">Location</span></span>

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

### <span data-ttu-id="b6512-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b6512-120">-Name</span></span>
<span data-ttu-id="b6512-121">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="b6512-121">WebApp Name</span></span>

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

### <span data-ttu-id="b6512-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6512-122">-ResourceGroupName</span></span>
<span data-ttu-id="b6512-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="b6512-123">Resource Group Name</span></span>

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

### <span data-ttu-id="b6512-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6512-124">CommonParameters</span></span>
<span data-ttu-id="b6512-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6512-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6512-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6512-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6512-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6512-127">INPUTS</span></span>

### <span data-ttu-id="b6512-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b6512-128">System.String</span></span>

## <span data-ttu-id="b6512-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6512-129">OUTPUTS</span></span>

### <span data-ttu-id="b6512-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="b6512-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b6512-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6512-131">NOTES</span></span>

## <span data-ttu-id="b6512-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6512-132">RELATED LINKS</span></span>

[<span data-ttu-id="b6512-133">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b6512-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="b6512-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b6512-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="b6512-135">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b6512-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="b6512-136">Anfang-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b6512-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="b6512-137">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b6512-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


