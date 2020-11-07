---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 36c336f516cf2621a64a6e0e353e93e7defa03b1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842235"
---
# <span data-ttu-id="01f71-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="01f71-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="01f71-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="01f71-102">SYNOPSIS</span></span>
<span data-ttu-id="01f71-103">Ruft die Informationen zu einem IotHub-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="01f71-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="01f71-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="01f71-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01f71-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01f71-105">DESCRIPTION</span></span>
<span data-ttu-id="01f71-106">Ruft die Informationen zu einem IotHub-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="01f71-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="01f71-107">Ein IotHub-Auftrag wird erstellt, wenn ein Import-oder Exportvorgang mithilfe der Befehle New-AzIotHubExportDevices oder New-AzIotHubImportDevices initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="01f71-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="01f71-108">Sie können entweder alle Aufträge auflisten oder die Aufträge nach der Auftrags-ID filtern.</span><span class="sxs-lookup"><span data-stu-id="01f71-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="01f71-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01f71-109">EXAMPLES</span></span>

### <span data-ttu-id="01f71-110">Beispiel 1 Auflisten aller Aufträge</span><span class="sxs-lookup"><span data-stu-id="01f71-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="01f71-111">Ruft alle Aufträge für das IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="01f71-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="01f71-112">Beispiel 2 Abrufen eines bestimmten Auftrags</span><span class="sxs-lookup"><span data-stu-id="01f71-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="01f71-113">Ruft Informationen über den Auftrag mit dem Bezeichner "3630fc31-4caa-43E8-a232-ea0577221cb2" für die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="01f71-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="01f71-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="01f71-114">PARAMETERS</span></span>

### <span data-ttu-id="01f71-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01f71-115">-DefaultProfile</span></span>
<span data-ttu-id="01f71-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="01f71-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01f71-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="01f71-117">-JobId</span></span>
<span data-ttu-id="01f71-118">Die Auftrags-ID.</span><span class="sxs-lookup"><span data-stu-id="01f71-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="01f71-119">-Name</span><span class="sxs-lookup"><span data-stu-id="01f71-119">-Name</span></span>
<span data-ttu-id="01f71-120">Der Name des viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="01f71-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="01f71-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01f71-121">-ResourceGroupName</span></span>
<span data-ttu-id="01f71-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="01f71-122">Resource Group Name</span></span>

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

### <span data-ttu-id="01f71-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f71-123">CommonParameters</span></span>
<span data-ttu-id="01f71-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01f71-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f71-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01f71-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f71-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="01f71-126">INPUTS</span></span>

### <span data-ttu-id="01f71-127">System. String</span><span class="sxs-lookup"><span data-stu-id="01f71-127">System.String</span></span>

## <span data-ttu-id="01f71-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="01f71-128">OUTPUTS</span></span>

### <span data-ttu-id="01f71-129">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="01f71-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="01f71-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="01f71-130">NOTES</span></span>

## <span data-ttu-id="01f71-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="01f71-131">RELATED LINKS</span></span>
