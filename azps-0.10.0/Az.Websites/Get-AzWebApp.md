---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: f86e0f18c7d793b5876a48c39b56b11c14b17546
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842796"
---
# <span data-ttu-id="0d613-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0d613-101">Get-AzWebApp</span></span>

## <span data-ttu-id="0d613-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d613-102">SYNOPSIS</span></span>
<span data-ttu-id="0d613-103">Ruft Azure Web Apps in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="0d613-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="0d613-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d613-104">SYNTAX</span></span>

### <span data-ttu-id="0d613-105">S1</span><span class="sxs-lookup"><span data-stu-id="0d613-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d613-106">S2</span><span class="sxs-lookup"><span data-stu-id="0d613-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <AppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d613-107">S3</span><span class="sxs-lookup"><span data-stu-id="0d613-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d613-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d613-108">DESCRIPTION</span></span>
<span data-ttu-id="0d613-109">Das Cmdlet " **Get-AzWebApp** " Ruft Informationen zu einer Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="0d613-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="0d613-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d613-110">EXAMPLES</span></span>

### <span data-ttu-id="0d613-111">Beispiel 1: Abrufen einer Web-App aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0d613-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="0d613-112">Dieser Befehl ruft die Web-App mit dem Namen ContosoSite ab, die der Ressourcengruppe Default-Web-westus angehört.</span><span class="sxs-lookup"><span data-stu-id="0d613-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="0d613-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d613-113">PARAMETERS</span></span>

### <span data-ttu-id="0d613-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0d613-114">-AppServicePlan</span></span>
<span data-ttu-id="0d613-115">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="0d613-115">App Service Plan object</span></span>

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

### <span data-ttu-id="0d613-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d613-116">-DefaultProfile</span></span>
<span data-ttu-id="0d613-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d613-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d613-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="0d613-118">-Location</span></span>
<span data-ttu-id="0d613-119">Lage</span><span class="sxs-lookup"><span data-stu-id="0d613-119">Location</span></span>

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

### <span data-ttu-id="0d613-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0d613-120">-Name</span></span>
<span data-ttu-id="0d613-121">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="0d613-121">WebApp Name</span></span>

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

### <span data-ttu-id="0d613-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d613-122">-ResourceGroupName</span></span>
<span data-ttu-id="0d613-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="0d613-123">Resource Group Name</span></span>

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

### <span data-ttu-id="0d613-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d613-124">CommonParameters</span></span>
<span data-ttu-id="0d613-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d613-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d613-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d613-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d613-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d613-127">INPUTS</span></span>

### <span data-ttu-id="0d613-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0d613-128">System.String</span></span>

## <span data-ttu-id="0d613-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d613-129">OUTPUTS</span></span>

### <span data-ttu-id="0d613-130">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="0d613-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="0d613-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d613-131">NOTES</span></span>

## <span data-ttu-id="0d613-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d613-132">RELATED LINKS</span></span>

[<span data-ttu-id="0d613-133">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0d613-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="0d613-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0d613-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="0d613-135">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0d613-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="0d613-136">Anfang-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0d613-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="0d613-137">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0d613-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


