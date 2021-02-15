---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 7c5c09f2379eb1c0306b89018732336b4223f5c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152929"
---
# <span data-ttu-id="20eec-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="20eec-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="20eec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20eec-102">SYNOPSIS</span></span>
<span data-ttu-id="20eec-103">Ruft die Informationen zu einem IotHub-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="20eec-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="20eec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20eec-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20eec-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20eec-105">DESCRIPTION</span></span>
<span data-ttu-id="20eec-106">Ruft die Informationen zu einem IotHub-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="20eec-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="20eec-107">Ein IotHub-Auftrag wird erstellt, wenn ein Import- oder Exportvorgang mithilfe der Befehle New-AzIotHubExportDevices oder New-AzIotHubImportDevices wird.</span><span class="sxs-lookup"><span data-stu-id="20eec-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="20eec-108">Sie können entweder alle Aufträge auflisten oder die Aufträge nach der Auftrags-ID filtern.</span><span class="sxs-lookup"><span data-stu-id="20eec-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="20eec-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="20eec-109">EXAMPLES</span></span>

### <span data-ttu-id="20eec-110">Beispiel 1: Auflisten aller Aufträge</span><span class="sxs-lookup"><span data-stu-id="20eec-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="20eec-111">Ruft alle Aufträge für IotHub namens "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="20eec-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="20eec-112">Beispiel 2: Erhalten eines bestimmten Auftrags</span><span class="sxs-lookup"><span data-stu-id="20eec-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="20eec-113">Ruft Informationen zu dem Auftrag mit dem Bezeichner "3630fc31-4caa-43e8-a232-ea0577221cb2" für IotHub namens "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="20eec-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="20eec-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20eec-114">PARAMETERS</span></span>

### <span data-ttu-id="20eec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20eec-115">-DefaultProfile</span></span>
<span data-ttu-id="20eec-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="20eec-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20eec-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="20eec-117">-JobId</span></span>
<span data-ttu-id="20eec-118">Die Auftrags-ID.</span><span class="sxs-lookup"><span data-stu-id="20eec-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="20eec-119">-Name</span><span class="sxs-lookup"><span data-stu-id="20eec-119">-Name</span></span>
<span data-ttu-id="20eec-120">Name des IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="20eec-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="20eec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20eec-121">-ResourceGroupName</span></span>
<span data-ttu-id="20eec-122">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="20eec-122">Resource Group Name</span></span>

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

### <span data-ttu-id="20eec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20eec-123">CommonParameters</span></span>
<span data-ttu-id="20eec-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20eec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20eec-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20eec-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20eec-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="20eec-126">INPUTS</span></span>

### <span data-ttu-id="20eec-127">System.String</span><span class="sxs-lookup"><span data-stu-id="20eec-127">System.String</span></span>

## <span data-ttu-id="20eec-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="20eec-128">OUTPUTS</span></span>

### <span data-ttu-id="20eec-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="20eec-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="20eec-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="20eec-130">NOTES</span></span>

## <span data-ttu-id="20eec-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="20eec-131">RELATED LINKS</span></span>
