---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 7c5c09f2379eb1c0306b89018732336b4223f5c9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306051"
---
# <span data-ttu-id="5c1d6-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="5c1d6-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="5c1d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c1d6-102">SYNOPSIS</span></span>
<span data-ttu-id="5c1d6-103">Ruft die Informationen zu einem IotHub-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="5c1d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c1d6-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c1d6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c1d6-105">DESCRIPTION</span></span>
<span data-ttu-id="5c1d6-106">Ruft die Informationen zu einem IotHub-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="5c1d6-107">Ein IotHub-Auftrag wird erstellt, wenn ein Import- oder Exportvorgang mithilfe der Befehle New-AzIotHubExportDevices oder New-AzIotHubImportDevices wird.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="5c1d6-108">Sie können entweder alle Aufträge auflisten oder die Aufträge nach der Auftrags-ID filtern.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="5c1d6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5c1d6-109">EXAMPLES</span></span>

### <span data-ttu-id="5c1d6-110">Beispiel 1: Auflisten aller Aufträge</span><span class="sxs-lookup"><span data-stu-id="5c1d6-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="5c1d6-111">Ruft alle Aufträge für IotHub namens "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="5c1d6-112">Beispiel 2: Erhalten eines bestimmten Auftrags</span><span class="sxs-lookup"><span data-stu-id="5c1d6-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="5c1d6-113">Ruft Informationen zu dem Auftrag mit dem Bezeichner "3630fc31-4caa-43e8-a232-ea0577221cb2" für IotHub namens "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="5c1d6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c1d6-114">PARAMETERS</span></span>

### <span data-ttu-id="5c1d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c1d6-115">-DefaultProfile</span></span>
<span data-ttu-id="5c1d6-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5c1d6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c1d6-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="5c1d6-117">-JobId</span></span>
<span data-ttu-id="5c1d6-118">Die Auftrags-ID.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="5c1d6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5c1d6-119">-Name</span></span>
<span data-ttu-id="5c1d6-120">Name des IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="5c1d6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c1d6-121">-ResourceGroupName</span></span>
<span data-ttu-id="5c1d6-122">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="5c1d6-122">Resource Group Name</span></span>

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

### <span data-ttu-id="5c1d6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c1d6-123">CommonParameters</span></span>
<span data-ttu-id="5c1d6-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c1d6-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c1d6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c1d6-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5c1d6-126">INPUTS</span></span>

### <span data-ttu-id="5c1d6-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5c1d6-127">System.String</span></span>

## <span data-ttu-id="5c1d6-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5c1d6-128">OUTPUTS</span></span>

### <span data-ttu-id="5c1d6-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="5c1d6-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="5c1d6-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5c1d6-130">NOTES</span></span>

## <span data-ttu-id="5c1d6-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5c1d6-131">RELATED LINKS</span></span>
