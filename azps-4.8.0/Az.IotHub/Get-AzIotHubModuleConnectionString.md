---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 30926eaad6447f109b1755d419be0b3931a76054
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175126"
---
# <span data-ttu-id="1307f-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="1307f-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="1307f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1307f-102">SYNOPSIS</span></span>
<span data-ttu-id="1307f-103">Besorgen Sie sich die Verbindungszeichenfolge eines Device-Moduls für Zielgeräte in einem viel Hub.</span><span class="sxs-lookup"><span data-stu-id="1307f-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="1307f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1307f-104">SYNTAX</span></span>

### <span data-ttu-id="1307f-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1307f-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1307f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1307f-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1307f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1307f-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1307f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1307f-108">DESCRIPTION</span></span>
<span data-ttu-id="1307f-109">Auflisten der Verbindungszeichenfolge aller Module oder eines angegebenen Moduls eines Ziel-viel-Geräts, das sich in einem Azure-viel-Hub befindet.</span><span class="sxs-lookup"><span data-stu-id="1307f-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="1307f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1307f-110">EXAMPLES</span></span>

### <span data-ttu-id="1307f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1307f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="1307f-112">Alle Module-Verbindungszeichenfolge eines Ziel-viel-Geräts in einem viel Hub anzeigen</span><span class="sxs-lookup"><span data-stu-id="1307f-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="1307f-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1307f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="1307f-114">Rufen Sie die Verbindungszeichenfolge des sekundären Moduls eines Ziel-viel-Geräts in einem viel Hub ab.</span><span class="sxs-lookup"><span data-stu-id="1307f-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="1307f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="1307f-115">PARAMETERS</span></span>

### <span data-ttu-id="1307f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1307f-116">-DefaultProfile</span></span>
<span data-ttu-id="1307f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1307f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1307f-118">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="1307f-118">-DeviceId</span></span>
<span data-ttu-id="1307f-119">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="1307f-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1307f-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1307f-120">-InputObject</span></span>
<span data-ttu-id="1307f-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="1307f-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1307f-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1307f-122">-IotHubName</span></span>
<span data-ttu-id="1307f-123">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="1307f-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1307f-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="1307f-124">-KeyType</span></span>
<span data-ttu-id="1307f-125">Gemeinsamer Zugriffsrichtlinien Schlüsseltyp für auth.</span><span class="sxs-lookup"><span data-stu-id="1307f-125">Shared access policy key type for auth.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1307f-126">-Modul-Nr</span><span class="sxs-lookup"><span data-stu-id="1307f-126">-ModuleId</span></span>
<span data-ttu-id="1307f-127">Ziel Modul-ID.</span><span class="sxs-lookup"><span data-stu-id="1307f-127">Target Module Id.</span></span>

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

### <span data-ttu-id="1307f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1307f-128">-ResourceGroupName</span></span>
<span data-ttu-id="1307f-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="1307f-129">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1307f-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1307f-130">-ResourceId</span></span>
<span data-ttu-id="1307f-131">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="1307f-131">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1307f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1307f-132">CommonParameters</span></span>
<span data-ttu-id="1307f-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1307f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1307f-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1307f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1307f-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1307f-135">INPUTS</span></span>

### <span data-ttu-id="1307f-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1307f-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1307f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1307f-137">System.String</span></span>

## <span data-ttu-id="1307f-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1307f-138">OUTPUTS</span></span>

### <span data-ttu-id="1307f-139">Microsoft. Azure. Commands. Management. IotHub. Models. PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="1307f-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="1307f-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="1307f-140">NOTES</span></span>

## <span data-ttu-id="1307f-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1307f-141">RELATED LINKS</span></span>
