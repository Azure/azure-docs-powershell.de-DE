---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006143"
---
# <span data-ttu-id="0a44a-101">Test-AzureName</span><span class="sxs-lookup"><span data-stu-id="0a44a-101">Test-AzureName</span></span>

## <span data-ttu-id="0a44a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a44a-102">SYNOPSIS</span></span>
<span data-ttu-id="0a44a-103">Testet, ob ein Microsoft Azure Cloud-Dienstname, ein Speicherdienst Name oder ein ServiceBus-Namespacename vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0a44a-103">Tests whether a Microsoft Azure cloud service name, storage service name or service bus namespace name exists or not.</span></span>

## <span data-ttu-id="0a44a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a44a-104">SYNTAX</span></span>

### <span data-ttu-id="0a44a-105">Dienst</span><span class="sxs-lookup"><span data-stu-id="0a44a-105">Service</span></span>
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0a44a-106">Speicher</span><span class="sxs-lookup"><span data-stu-id="0a44a-106">Storage</span></span>
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0a44a-107">ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="0a44a-107">ServiceBusNamespace</span></span>
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0a44a-108">Website</span><span class="sxs-lookup"><span data-stu-id="0a44a-108">Website</span></span>
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0a44a-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a44a-109">DESCRIPTION</span></span>
<span data-ttu-id="0a44a-110">Wenn der Name vorhanden ist, gibt das Cmdlet $true zurück.</span><span class="sxs-lookup"><span data-stu-id="0a44a-110">If the name exists, the cmdlet returns $True.</span></span>
<span data-ttu-id="0a44a-111">Wenn der Name nicht vorhanden ist, wird $false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0a44a-111">If the name does not exist, it returns $False.</span></span>

## <span data-ttu-id="0a44a-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a44a-112">EXAMPLES</span></span>

### <span data-ttu-id="0a44a-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0a44a-113">Example 1</span></span>
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

<span data-ttu-id="0a44a-114">Dieser Befehl testet, ob es sich bei dem "MyNameService1" um einen vorhandenen Microsoft Azure Cloud-Dienstnamen handelt.</span><span class="sxs-lookup"><span data-stu-id="0a44a-114">This command tests to see if the "MyNameService1" is an existing Microsoft Azure cloud service name.</span></span>

### <span data-ttu-id="0a44a-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0a44a-115">Example 2</span></span>
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

<span data-ttu-id="0a44a-116">Dieser Befehl testet, ob es sich bei dem "mystorename1" um einen vorhandenen Microsoft Azure-Speicherdienst Namen handelt.</span><span class="sxs-lookup"><span data-stu-id="0a44a-116">This command tests to see if the "mystorename1" is an existing Microsoft Azure storage service name.</span></span>

### <span data-ttu-id="0a44a-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0a44a-117">Example 3</span></span>
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

<span data-ttu-id="0a44a-118">Dieser Befehl testet, ob es sich bei dem "MyNamespace" um einen vorhandenen Microsoft Azure Service Bus-Namespacenamen handelt.</span><span class="sxs-lookup"><span data-stu-id="0a44a-118">This command tests to see if the "mynamespace" is an existing Microsoft Azure service bus namespace name.</span></span>

## <span data-ttu-id="0a44a-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a44a-119">PARAMETERS</span></span>

### <span data-ttu-id="0a44a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0a44a-120">-Name</span></span>
<span data-ttu-id="0a44a-121">Gibt den Namen des Dienst-oder speicherkontos an, das getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a44a-121">Specifies the name of the service or storage account to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a44a-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="0a44a-122">-Profile</span></span>
<span data-ttu-id="0a44a-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0a44a-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0a44a-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0a44a-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a44a-125">-Service</span><span class="sxs-lookup"><span data-stu-id="0a44a-125">-Service</span></span>
<span data-ttu-id="0a44a-126">Gibt an, dass ein vorhandenes Dienstkonto getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a44a-126">Specifies to test for an existing service account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a44a-127">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="0a44a-127">-ServiceBusNamespace</span></span>
<span data-ttu-id="0a44a-128">Gibt an, dass ein vorhandener ServiceBus-Namespace getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a44a-128">Specifies to test for an existing service bus namespace.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a44a-129">-Speicher</span><span class="sxs-lookup"><span data-stu-id="0a44a-129">-Storage</span></span>
<span data-ttu-id="0a44a-130">Gibt an, dass ein vorhandenes Speicherkonto getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a44a-130">Specifies to test for an existing storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a44a-131">-Website</span><span class="sxs-lookup"><span data-stu-id="0a44a-131">-Website</span></span>
<span data-ttu-id="0a44a-132">Gibt an, dass eine vorhandene Website getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a44a-132">Specifies to test for an existing website.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Website
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a44a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a44a-133">CommonParameters</span></span>
<span data-ttu-id="0a44a-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a44a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a44a-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a44a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a44a-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a44a-136">INPUTS</span></span>

## <span data-ttu-id="0a44a-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a44a-137">OUTPUTS</span></span>

## <span data-ttu-id="0a44a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a44a-138">NOTES</span></span>
* <span data-ttu-id="0a44a-139">Node-dev, php-dev, python-dev</span><span class="sxs-lookup"><span data-stu-id="0a44a-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="0a44a-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a44a-140">RELATED LINKS</span></span>

