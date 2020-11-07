---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
ms.openlocfilehash: 684b892d2c2cc995e12ae6327541f13428da270f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664602"
---
# <span data-ttu-id="3ff5f-101">Get-AzureRmIotHubJob</span><span class="sxs-lookup"><span data-stu-id="3ff5f-101">Get-AzureRmIotHubJob</span></span>

## <span data-ttu-id="3ff5f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3ff5f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff5f-103">Ruft die Informationen zu einem IotHub-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="3ff5f-103">Gets the information about an IotHub job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ff5f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ff5f-104">SYNTAX</span></span>

```
Get-AzureRmIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ff5f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3ff5f-105">DESCRIPTION</span></span>
<span data-ttu-id="3ff5f-106">Ruft die Informationen zu einem IotHub-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="3ff5f-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="3ff5f-107">Ein IotHub-Auftrag wird erstellt, wenn ein Import-oder Exportvorgang mithilfe der Befehle New-AzureRmIotHubExportDevices oder New-AzureRmIotHubImportDevices initialted wird.</span><span class="sxs-lookup"><span data-stu-id="3ff5f-107">An IotHub Job gets created when an import or export operation is initialted using the New-AzureRmIotHubExportDevices or New-AzureRmIotHubImportDevices commands.</span></span>
<span data-ttu-id="3ff5f-108">Sie können entweder alle Aufträge auflisten oder die Aufträge nach der Auftrags-ID filtern.</span><span class="sxs-lookup"><span data-stu-id="3ff5f-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="3ff5f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ff5f-109">EXAMPLES</span></span>

### <span data-ttu-id="3ff5f-110">Beispiel 1 Auflisten aller Aufträge</span><span class="sxs-lookup"><span data-stu-id="3ff5f-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="3ff5f-111">Ruft alle Aufträge für das IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="3ff5f-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="3ff5f-112">Beispiel 2 Abrufen eines bestimmten Auftrags</span><span class="sxs-lookup"><span data-stu-id="3ff5f-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="3ff5f-113">Ruft Informationen über den Auftrag mit dem Bezeichner "3630fc31-4caa-43E8-a232-ea0577221cb2" für die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="3ff5f-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="3ff5f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ff5f-114">PARAMETERS</span></span>

### <span data-ttu-id="3ff5f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff5f-115">-DefaultProfile</span></span>
<span data-ttu-id="3ff5f-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3ff5f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ff5f-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="3ff5f-117">-JobId</span></span>
<span data-ttu-id="3ff5f-118">Die Auftrags-ID.</span><span class="sxs-lookup"><span data-stu-id="3ff5f-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="3ff5f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3ff5f-119">-Name</span></span>
<span data-ttu-id="3ff5f-120">Der Name des viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="3ff5f-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="3ff5f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ff5f-121">-ResourceGroupName</span></span>
<span data-ttu-id="3ff5f-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="3ff5f-122">Resource Group Name</span></span>

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

### <span data-ttu-id="3ff5f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff5f-123">CommonParameters</span></span>
<span data-ttu-id="3ff5f-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ff5f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff5f-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ff5f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff5f-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3ff5f-126">INPUTS</span></span>

### <span data-ttu-id="3ff5f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3ff5f-127">System.String</span></span>

## <span data-ttu-id="3ff5f-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3ff5f-128">OUTPUTS</span></span>

### <span data-ttu-id="3ff5f-129">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="3ff5f-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="3ff5f-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="3ff5f-130">NOTES</span></span>

## <span data-ttu-id="3ff5f-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3ff5f-131">RELATED LINKS</span></span>
