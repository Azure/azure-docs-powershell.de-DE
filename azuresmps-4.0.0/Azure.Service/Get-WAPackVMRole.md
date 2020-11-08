---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7EB9FE4-BDEB-43A5-B6D3-FEAB16BC2711
online version: ''
schema: 2.0.0
ms.openlocfilehash: 388277115281cbbacfb634ebdac5cdd9aa86b709
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007620"
---
# <span data-ttu-id="2547a-101">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="2547a-101">Get-WAPackVMRole</span></span>

## <span data-ttu-id="2547a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2547a-102">SYNOPSIS</span></span>

## <span data-ttu-id="2547a-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="2547a-103">SYNTAX</span></span>

### <span data-ttu-id="2547a-104">Leer (Standard)</span><span class="sxs-lookup"><span data-stu-id="2547a-104">Empty (Default)</span></span>
```
Get-WAPackVMRole [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2547a-105">FromName</span><span class="sxs-lookup"><span data-stu-id="2547a-105">FromName</span></span>
```
Get-WAPackVMRole -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2547a-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="2547a-106">FromCloudService</span></span>
```
Get-WAPackVMRole -Name <String> -CloudServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2547a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2547a-107">DESCRIPTION</span></span>
<span data-ttu-id="2547a-108">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="2547a-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="2547a-109">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2547a-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2547a-110">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2547a-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="2547a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2547a-111">EXAMPLES</span></span>

### <span data-ttu-id="2547a-112">Beispiel 1: Abrufen einer Rolle des virtuellen Computers (erstellt über das Portal)</span><span class="sxs-lookup"><span data-stu-id="2547a-112">Example 1: Get a virtual machine role (created through the portal)</span></span>
```
PS C:\> Get-WAPackVMRole -Name "ContosoVMRole01"
```

<span data-ttu-id="2547a-113">Dieser Befehl ruft eine Rolle des virtuellen Computers ab, die über das Portal mit dem Namen ContosoVMRole01 erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2547a-113">This command gets a virtual machine role which has been created through the portal named ContosoVMRole01.</span></span>

### <span data-ttu-id="2547a-114">Beispiel 2: Abrufen einer Rolle für einen virtuellen Computer mithilfe eines Namens und eines Cloud-Dienst namens</span><span class="sxs-lookup"><span data-stu-id="2547a-114">Example 2: Get a virtual machine role by using a name and a cloud service name</span></span>
```
PS C:\> Get-WAPackVMRole -CloudServiceName "ContosoCloudService01" -Name "ContosoVMRole02"
```

<span data-ttu-id="2547a-115">Dieser Befehl ruft eine Rolle des virtuellen Computers mit dem Namen ContosoVMRole02 auf, die sich auf einem clouddienst mit dem Namen ContosoCloudService01 befindet.</span><span class="sxs-lookup"><span data-stu-id="2547a-115">This command gets a virtual machine role named ContosoVMRole02 which stand on a cloud service named ContosoCloudService01.</span></span>

### <span data-ttu-id="2547a-116">Beispiel 3: Abrufen der gesamten Rolle eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="2547a-116">Example 3: Get all virtual machine role</span></span>
```
PS C:\> Get-WAPackVMRole
```

<span data-ttu-id="2547a-117">Dieser Befehl ruft alle vorhandenen virtuellen Computerrollen ab.</span><span class="sxs-lookup"><span data-stu-id="2547a-117">This command gets all existing virtual machine role.</span></span>

## <span data-ttu-id="2547a-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="2547a-118">PARAMETERS</span></span>

### <span data-ttu-id="2547a-119">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="2547a-119">-CloudServiceName</span></span>
<span data-ttu-id="2547a-120">Gibt den Namen des Cloud-Diensts der Rolle des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="2547a-120">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2547a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2547a-121">-Name</span></span>
<span data-ttu-id="2547a-122">Gibt den Namen einer Rolle für einen virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="2547a-122">Specifies the name of a virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromName, FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2547a-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="2547a-123">-Profile</span></span>
<span data-ttu-id="2547a-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="2547a-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2547a-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="2547a-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2547a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2547a-126">CommonParameters</span></span>
<span data-ttu-id="2547a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2547a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2547a-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2547a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2547a-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2547a-129">INPUTS</span></span>

## <span data-ttu-id="2547a-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2547a-130">OUTPUTS</span></span>

## <span data-ttu-id="2547a-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="2547a-131">NOTES</span></span>

## <span data-ttu-id="2547a-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2547a-132">RELATED LINKS</span></span>

[<span data-ttu-id="2547a-133">Neu – WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="2547a-133">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="2547a-134">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="2547a-134">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="2547a-135">Satz-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="2547a-135">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


