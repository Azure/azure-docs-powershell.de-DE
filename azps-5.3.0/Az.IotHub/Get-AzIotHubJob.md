---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 7c5c09f2379eb1c0306b89018732336b4223f5c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472407"
---
# <span data-ttu-id="2085e-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="2085e-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="2085e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2085e-102">SYNOPSIS</span></span>
<span data-ttu-id="2085e-103">Ruft die Informationen zu einem IotHub-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="2085e-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="2085e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2085e-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2085e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2085e-105">DESCRIPTION</span></span>
<span data-ttu-id="2085e-106">Ruft die Informationen zu einem IotHub-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="2085e-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="2085e-107">Ein IotHub-Auftrag wird erstellt, wenn ein Import- oder Exportvorgang mithilfe der Befehle New-AzIotHubExportDevices oder New-AzIotHubImportDevices wird.</span><span class="sxs-lookup"><span data-stu-id="2085e-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="2085e-108">Sie können entweder alle Aufträge auflisten oder die Aufträge nach der Auftrags-ID filtern.</span><span class="sxs-lookup"><span data-stu-id="2085e-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="2085e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2085e-109">EXAMPLES</span></span>

### <span data-ttu-id="2085e-110">Beispiel 1: Auflisten aller Aufträge</span><span class="sxs-lookup"><span data-stu-id="2085e-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="2085e-111">Ruft alle Aufträge für IotHub namens "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="2085e-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="2085e-112">Beispiel 2: Erhalten eines bestimmten Auftrags</span><span class="sxs-lookup"><span data-stu-id="2085e-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="2085e-113">Ruft Informationen zu dem Auftrag mit dem Bezeichner "3630fc31-4caa-43e8-a232-ea0577221cb2" für IotHub namens "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="2085e-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="2085e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2085e-114">PARAMETERS</span></span>

### <span data-ttu-id="2085e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2085e-115">-DefaultProfile</span></span>
<span data-ttu-id="2085e-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2085e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2085e-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="2085e-117">-JobId</span></span>
<span data-ttu-id="2085e-118">Die Auftrags-ID.</span><span class="sxs-lookup"><span data-stu-id="2085e-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="2085e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2085e-119">-Name</span></span>
<span data-ttu-id="2085e-120">Name des IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="2085e-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="2085e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2085e-121">-ResourceGroupName</span></span>
<span data-ttu-id="2085e-122">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="2085e-122">Resource Group Name</span></span>

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

### <span data-ttu-id="2085e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2085e-123">CommonParameters</span></span>
<span data-ttu-id="2085e-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2085e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2085e-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2085e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2085e-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2085e-126">INPUTS</span></span>

### <span data-ttu-id="2085e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="2085e-127">System.String</span></span>

## <span data-ttu-id="2085e-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2085e-128">OUTPUTS</span></span>

### <span data-ttu-id="2085e-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="2085e-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="2085e-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2085e-130">NOTES</span></span>

## <span data-ttu-id="2085e-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2085e-131">RELATED LINKS</span></span>
