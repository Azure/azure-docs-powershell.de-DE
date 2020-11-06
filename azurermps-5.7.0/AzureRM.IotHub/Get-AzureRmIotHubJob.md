---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
ms.openlocfilehash: daacefe94d694a6d6288e4c1ccd0f6b05ad1e582
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496525"
---
# <span data-ttu-id="eebfa-101">Get-AzureRmIotHubJob</span><span class="sxs-lookup"><span data-stu-id="eebfa-101">Get-AzureRmIotHubJob</span></span>

## <span data-ttu-id="eebfa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eebfa-102">SYNOPSIS</span></span>
<span data-ttu-id="eebfa-103">Ruft die Informationen zu einem IotHub-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="eebfa-103">Gets the information about an IotHub job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eebfa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eebfa-104">SYNTAX</span></span>

```
Get-AzureRmIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eebfa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eebfa-105">DESCRIPTION</span></span>
<span data-ttu-id="eebfa-106">Ruft die Informationen zu einem IotHub-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="eebfa-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="eebfa-107">Ein IotHub-Auftrag wird erstellt, wenn ein Import-oder Exportvorgang mithilfe der Befehle New-AzureRmIotHubExportDevices oder New-AzureRmIotHubImportDevices initialted wird.</span><span class="sxs-lookup"><span data-stu-id="eebfa-107">An IotHub Job gets created when an import or export operation is initialted using the New-AzureRmIotHubExportDevices or New-AzureRmIotHubImportDevices commands.</span></span>
<span data-ttu-id="eebfa-108">Sie können entweder alle Aufträge auflisten oder die Aufträge nach der Auftrags-ID filtern.</span><span class="sxs-lookup"><span data-stu-id="eebfa-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="eebfa-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eebfa-109">EXAMPLES</span></span>

### <span data-ttu-id="eebfa-110">Beispiel 1 Auflisten aller Aufträge</span><span class="sxs-lookup"><span data-stu-id="eebfa-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="eebfa-111">Ruft alle Aufträge für das IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="eebfa-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="eebfa-112">Beispiel 2 Abrufen eines bestimmten Auftrags</span><span class="sxs-lookup"><span data-stu-id="eebfa-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="eebfa-113">Ruft Informationen über den Auftrag mit dem Bezeichner "3630fc31-4caa-43E8-a232-ea0577221cb2" für die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="eebfa-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="eebfa-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="eebfa-114">PARAMETERS</span></span>

### <span data-ttu-id="eebfa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eebfa-115">-DefaultProfile</span></span>
<span data-ttu-id="eebfa-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="eebfa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eebfa-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="eebfa-117">-JobId</span></span>
<span data-ttu-id="eebfa-118">Die Auftrags-ID.</span><span class="sxs-lookup"><span data-stu-id="eebfa-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="eebfa-119">-Name</span><span class="sxs-lookup"><span data-stu-id="eebfa-119">-Name</span></span>
<span data-ttu-id="eebfa-120">Der Name des viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="eebfa-120">Name of the IoT hub.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eebfa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eebfa-121">-ResourceGroupName</span></span>
<span data-ttu-id="eebfa-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="eebfa-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eebfa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eebfa-123">CommonParameters</span></span>
<span data-ttu-id="eebfa-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eebfa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eebfa-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eebfa-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eebfa-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eebfa-126">INPUTS</span></span>

### <span data-ttu-id="eebfa-127">System. String</span><span class="sxs-lookup"><span data-stu-id="eebfa-127">System.String</span></span>

## <span data-ttu-id="eebfa-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eebfa-128">OUTPUTS</span></span>

### <span data-ttu-id="eebfa-129">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="eebfa-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>
<span data-ttu-id="eebfa-130">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="eebfa-130">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="eebfa-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="eebfa-131">NOTES</span></span>

## <span data-ttu-id="eebfa-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eebfa-132">RELATED LINKS</span></span>

