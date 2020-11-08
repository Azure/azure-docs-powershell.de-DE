---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: 74c518d4713c19c7a1bb7b7d0b3341e164e22c35
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180136"
---
# <span data-ttu-id="f912e-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="f912e-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="f912e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f912e-102">SYNOPSIS</span></span>
<span data-ttu-id="f912e-103">Ruft gelöschte Web-Apps im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="f912e-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="f912e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f912e-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f912e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f912e-105">DESCRIPTION</span></span>
<span data-ttu-id="f912e-106">Das Cmdlet " **Get-AzDeletedWebApp** " gibt alle gelöschten Webanwendungen im Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="f912e-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="f912e-107">Gelöschte Apps können optional nach Ressourcengruppe, Name und Steckplatz gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="f912e-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="f912e-108">Es können mehr als eine gelöschte App mit demselben Namen und derselben Ressourcengruppe vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f912e-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="f912e-109">Überprüfen Sie den Löschvorgang, um gelöschte apps zu unterscheiden, die denselben Namen haben.</span><span class="sxs-lookup"><span data-stu-id="f912e-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="f912e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f912e-110">EXAMPLES</span></span>

### <span data-ttu-id="f912e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f912e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="f912e-112">Dieser Befehl ruft die gelöschten apps mit dem Namen ContosoSite ab, die zu der Ressourcengruppe Standard-Web-westus gehören.</span><span class="sxs-lookup"><span data-stu-id="f912e-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f912e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f912e-113">PARAMETERS</span></span>

### <span data-ttu-id="f912e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f912e-114">-DefaultProfile</span></span>
<span data-ttu-id="f912e-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f912e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f912e-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="f912e-116">-Location</span></span>
<span data-ttu-id="f912e-117">Der Speicherort der gelöschten app.</span><span class="sxs-lookup"><span data-stu-id="f912e-117">The location of the deleted app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f912e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f912e-118">-Name</span></span>
<span data-ttu-id="f912e-119">Der Name der Web-App.</span><span class="sxs-lookup"><span data-stu-id="f912e-119">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f912e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f912e-120">-ResourceGroupName</span></span>
<span data-ttu-id="f912e-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f912e-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f912e-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="f912e-122">-Slot</span></span>
<span data-ttu-id="f912e-123">Der Name des Web App-Slots.</span><span class="sxs-lookup"><span data-stu-id="f912e-123">The name of the web app slot.</span></span>

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

### <span data-ttu-id="f912e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f912e-124">CommonParameters</span></span>
<span data-ttu-id="f912e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f912e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f912e-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f912e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f912e-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f912e-127">INPUTS</span></span>

### <span data-ttu-id="f912e-128">Keine</span><span class="sxs-lookup"><span data-stu-id="f912e-128">None</span></span>

## <span data-ttu-id="f912e-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f912e-129">OUTPUTS</span></span>

### <span data-ttu-id="f912e-130">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="f912e-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="f912e-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="f912e-131">NOTES</span></span>

## <span data-ttu-id="f912e-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f912e-132">RELATED LINKS</span></span>

[<span data-ttu-id="f912e-133">Wiederherstellen – AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="f912e-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)