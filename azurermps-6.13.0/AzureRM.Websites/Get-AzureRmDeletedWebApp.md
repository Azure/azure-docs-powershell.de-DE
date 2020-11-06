---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
ms.openlocfilehash: 75ad4e1fabb511ee4ca3cff024389a8e826aeadd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497182"
---
# <span data-ttu-id="1e31e-101">Get-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1e31e-101">Get-AzureRmDeletedWebApp</span></span>

## <span data-ttu-id="1e31e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e31e-102">SYNOPSIS</span></span>
<span data-ttu-id="1e31e-103">Ruft gelöschte Web-Apps im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="1e31e-103">Gets deleted web apps in the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e31e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e31e-104">SYNTAX</span></span>

```
Get-AzureRmDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e31e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e31e-105">DESCRIPTION</span></span>
<span data-ttu-id="1e31e-106">Das Cmdlet " **Get-AzureRmDeletedWebApp** " gibt alle gelöschten Webanwendungen im Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="1e31e-106">The **Get-AzureRmDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="1e31e-107">Gelöschte Apps können optional nach Ressourcengruppe, Name und Steckplatz gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="1e31e-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="1e31e-108">Es können mehr als eine gelöschte App mit demselben Namen und derselben Ressourcengruppe vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="1e31e-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="1e31e-109">Überprüfen Sie den Löschvorgang, um gelöschte apps zu unterscheiden, die denselben Namen haben.</span><span class="sxs-lookup"><span data-stu-id="1e31e-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="1e31e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e31e-110">EXAMPLES</span></span>

### <span data-ttu-id="1e31e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1e31e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="1e31e-112">Dieser Befehl ruft die gelöschten apps mit dem Namen ContosoSite ab, die zu der Ressourcengruppe Standard-Web-westus gehören.</span><span class="sxs-lookup"><span data-stu-id="1e31e-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="1e31e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e31e-113">PARAMETERS</span></span>

### <span data-ttu-id="1e31e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e31e-114">-DefaultProfile</span></span>
<span data-ttu-id="1e31e-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1e31e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e31e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1e31e-116">-Name</span></span>
<span data-ttu-id="1e31e-117">Der Name der Web-App.</span><span class="sxs-lookup"><span data-stu-id="1e31e-117">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e31e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e31e-118">-ResourceGroupName</span></span>
<span data-ttu-id="1e31e-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1e31e-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e31e-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="1e31e-120">-Slot</span></span>
<span data-ttu-id="1e31e-121">Der Name des Web App-Slots.</span><span class="sxs-lookup"><span data-stu-id="1e31e-121">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e31e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e31e-122">CommonParameters</span></span>
<span data-ttu-id="1e31e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e31e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1e31e-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e31e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e31e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e31e-125">INPUTS</span></span>

### <span data-ttu-id="1e31e-126">Keine</span><span class="sxs-lookup"><span data-stu-id="1e31e-126">None</span></span>

## <span data-ttu-id="1e31e-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e31e-127">OUTPUTS</span></span>

### <span data-ttu-id="1e31e-128">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1e31e-128">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="1e31e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e31e-129">NOTES</span></span>

## <span data-ttu-id="1e31e-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e31e-130">RELATED LINKS</span></span>

[<span data-ttu-id="1e31e-131">Wiederherstellen – AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1e31e-131">Restore-AzureRmDeletedWebApp</span></span>](./Restore-AzureRmDeletedWebApp.md)
