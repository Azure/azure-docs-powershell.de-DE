---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: 74c518d4713c19c7a1bb7b7d0b3341e164e22c35
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291496"
---
# <span data-ttu-id="13611-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="13611-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="13611-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13611-102">SYNOPSIS</span></span>
<span data-ttu-id="13611-103">Ruft gelöschte Web Apps im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="13611-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="13611-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13611-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13611-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13611-105">DESCRIPTION</span></span>
<span data-ttu-id="13611-106">Das **Cmdlet "Get-AzDeletedWebApp"** gibt alle gelöschten Web Apps im Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="13611-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="13611-107">Gelöschte Apps können optional nach Ressourcengruppe, Name und Slot gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="13611-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="13611-108">Es kann mehrere gelöschte Apps mit demselben Namen und derselben Ressourcengruppe geben.</span><span class="sxs-lookup"><span data-stu-id="13611-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="13611-109">Überprüfen Sie das Löschzeit-Kontrollkästchen, um gelöschte Apps mit demselben Namen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="13611-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="13611-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="13611-110">EXAMPLES</span></span>

### <span data-ttu-id="13611-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="13611-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="13611-112">Dieser Befehl ruft die gelöschten Apps namens "ContosoSite" ab, die zur Ressourcengruppe "Default-Web-WestUS" gehören.</span><span class="sxs-lookup"><span data-stu-id="13611-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="13611-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13611-113">PARAMETERS</span></span>

### <span data-ttu-id="13611-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13611-114">-DefaultProfile</span></span>
<span data-ttu-id="13611-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13611-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13611-116">-Location</span><span class="sxs-lookup"><span data-stu-id="13611-116">-Location</span></span>
<span data-ttu-id="13611-117">Der Speicherort der gelöschten App.</span><span class="sxs-lookup"><span data-stu-id="13611-117">The location of the deleted app.</span></span>

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

### <span data-ttu-id="13611-118">-Name</span><span class="sxs-lookup"><span data-stu-id="13611-118">-Name</span></span>
<span data-ttu-id="13611-119">Der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="13611-119">The name of the web app.</span></span>

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

### <span data-ttu-id="13611-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13611-120">-ResourceGroupName</span></span>
<span data-ttu-id="13611-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="13611-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="13611-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="13611-122">-Slot</span></span>
<span data-ttu-id="13611-123">Der Name des Web-App-Slot.</span><span class="sxs-lookup"><span data-stu-id="13611-123">The name of the web app slot.</span></span>

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

### <span data-ttu-id="13611-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13611-124">CommonParameters</span></span>
<span data-ttu-id="13611-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13611-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13611-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13611-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13611-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="13611-127">INPUTS</span></span>

### <span data-ttu-id="13611-128">Keine</span><span class="sxs-lookup"><span data-stu-id="13611-128">None</span></span>

## <span data-ttu-id="13611-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="13611-129">OUTPUTS</span></span>

### <span data-ttu-id="13611-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="13611-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="13611-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="13611-131">NOTES</span></span>

## <span data-ttu-id="13611-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="13611-132">RELATED LINKS</span></span>

[<span data-ttu-id="13611-133">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="13611-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)