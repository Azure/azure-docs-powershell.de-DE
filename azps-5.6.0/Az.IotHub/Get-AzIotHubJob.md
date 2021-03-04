---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 191b5a75a5f9f581308c8d5aa214fe4f2ae84851
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936864"
---
# <span data-ttu-id="81162-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="81162-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="81162-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81162-102">SYNOPSIS</span></span>
<span data-ttu-id="81162-103">Ruft die Informationen zu einem IotHub-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="81162-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="81162-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81162-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81162-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81162-105">DESCRIPTION</span></span>
<span data-ttu-id="81162-106">Ruft die Informationen zu einem IotHub-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="81162-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="81162-107">Ein IotHub-Auftrag wird erstellt, wenn ein Import- oder Exportvorgang mithilfe der Befehle New-AzIotHubExportDevices oder New-AzIotHubImportDevices initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="81162-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="81162-108">Sie können entweder alle Aufträge auflisten oder die Aufträge nach dem Auftragsbezeichner filtern.</span><span class="sxs-lookup"><span data-stu-id="81162-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="81162-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="81162-109">EXAMPLES</span></span>

### <span data-ttu-id="81162-110">Beispiel 1: Alle Aufträge auflisten</span><span class="sxs-lookup"><span data-stu-id="81162-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="81162-111">Ruft alle Aufträge für den IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="81162-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="81162-112">Beispiel 2 : Einen bestimmten Auftrag erhalten</span><span class="sxs-lookup"><span data-stu-id="81162-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="81162-113">Ruft Informationen zum Auftrag mit dem Bezeichner "3630fc31-4caa-43e8-a232-ea0577221cb2" für den IotHub namens "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="81162-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="81162-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="81162-114">PARAMETERS</span></span>

### <span data-ttu-id="81162-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81162-115">-DefaultProfile</span></span>
<span data-ttu-id="81162-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="81162-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81162-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="81162-117">-JobId</span></span>
<span data-ttu-id="81162-118">Der Auftragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="81162-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="81162-119">-Name</span><span class="sxs-lookup"><span data-stu-id="81162-119">-Name</span></span>
<span data-ttu-id="81162-120">Name des IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="81162-120">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81162-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81162-121">-ResourceGroupName</span></span>
<span data-ttu-id="81162-122">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="81162-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81162-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81162-123">CommonParameters</span></span>
<span data-ttu-id="81162-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81162-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81162-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81162-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81162-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="81162-126">INPUTS</span></span>

### <span data-ttu-id="81162-127">System.String</span><span class="sxs-lookup"><span data-stu-id="81162-127">System.String</span></span>

## <span data-ttu-id="81162-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="81162-128">OUTPUTS</span></span>

### <span data-ttu-id="81162-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="81162-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="81162-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="81162-130">NOTES</span></span>

## <span data-ttu-id="81162-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="81162-131">RELATED LINKS</span></span>
