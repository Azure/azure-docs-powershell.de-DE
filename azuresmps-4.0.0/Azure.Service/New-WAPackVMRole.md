---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6617AA59-CDD1-4BA9-84A7-F3914BF1D4B7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14e201dc916f15b63b0e825f4ca2e37015aaa9bc
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007596"
---
# <span data-ttu-id="922fc-101">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="922fc-101">New-WAPackVMRole</span></span>

## <span data-ttu-id="922fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="922fc-102">SYNOPSIS</span></span>
<span data-ttu-id="922fc-103">Erstellt eine Rolle für einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="922fc-103">Creates a virtual machine role.</span></span>

## <span data-ttu-id="922fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="922fc-104">SYNTAX</span></span>

### <span data-ttu-id="922fc-105">QuickCreate (Standard)</span><span class="sxs-lookup"><span data-stu-id="922fc-105">QuickCreate (Default)</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="922fc-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="922fc-106">FromCloudService</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 -CloudService <CloudService> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="922fc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="922fc-107">DESCRIPTION</span></span>
<span data-ttu-id="922fc-108">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="922fc-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="922fc-109">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="922fc-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="922fc-110">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="922fc-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="922fc-111">Das Cmdlet **New-WAPackVMRole** erstellt eine Rolle für einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="922fc-111">The **New-WAPackVMRole** cmdlet creates a virtual machine role.</span></span>

## <span data-ttu-id="922fc-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="922fc-112">EXAMPLES</span></span>

### <span data-ttu-id="922fc-113">Beispiel 1: Erstellen einer virtuellen Computerrolle (emulieren des WAP-Verhaltens)</span><span class="sxs-lookup"><span data-stu-id="922fc-113">Example 1: Create a virtual machine role (emulating WAP behavior)</span></span>
```
PS C:\> New-WAPackVMRole -Name "ContosoVMRole01" -Label "ContosoVMRoleLabel01" -ResourceDefinition $resdef
```

<span data-ttu-id="922fc-114">Da wir keinen clouddienst angeben (emulieren des WAP-Verhaltens), wird mit dem Befehl ein clouddienst für uns erstellt, der den gleichen Namen wie die Rolle des virtuellen Computers hat.</span><span class="sxs-lookup"><span data-stu-id="922fc-114">Since we do not specify any cloud service (emulating WAP behavior), the command will create a cloud service for us which will have the same name as the virtual machine role.</span></span>
<span data-ttu-id="922fc-115">In diesem Fall wird mit dem folgenden Befehl eine Rolle für einen virtuellen Computer mit dem Namen ContosoVMRole01, Label ContosoVMRoleLabel01, erstellt.</span><span class="sxs-lookup"><span data-stu-id="922fc-115">In this case, the following command will create a virtual machine role with the name ContosoVMRole01, label ContosoVMRoleLabel01.</span></span>
<span data-ttu-id="922fc-116">Beachten Sie, dass die hier verwendete Ressourcendefinition manuell erstellt werden muss, wenn PowerShell verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="922fc-116">Note that the resource definition being used here has to be manually created though PowerShell.</span></span>

## <span data-ttu-id="922fc-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="922fc-117">PARAMETERS</span></span>

### <span data-ttu-id="922fc-118">-CloudService</span><span class="sxs-lookup"><span data-stu-id="922fc-118">-CloudService</span></span>
<span data-ttu-id="922fc-119">Gibt einen cloudbasierten Dienst für die Rolle des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="922fc-119">Specifies a cloud service for the virtual machine role.</span></span>

```yaml
Type: CloudService
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="922fc-120">-Label</span><span class="sxs-lookup"><span data-stu-id="922fc-120">-Label</span></span>
<span data-ttu-id="922fc-121">Gibt eine Bezeichnung für die Rolle des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="922fc-121">Specifies a label for the virtual machine role.</span></span>

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

### <span data-ttu-id="922fc-122">-Name</span><span class="sxs-lookup"><span data-stu-id="922fc-122">-Name</span></span>
<span data-ttu-id="922fc-123">Gibt einen Namen für die Rolle des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="922fc-123">Specifies a name for the virtual machine role.</span></span>

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

### <span data-ttu-id="922fc-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="922fc-124">-Profile</span></span>
<span data-ttu-id="922fc-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="922fc-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="922fc-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="922fc-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="922fc-127">-ResourceDefinition</span><span class="sxs-lookup"><span data-stu-id="922fc-127">-ResourceDefinition</span></span>
<span data-ttu-id="922fc-128">Gibt eine Ressourcendefinition für die Rolle des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="922fc-128">Specifies a resource definition for the virtual machine role.</span></span>

```yaml
Type: VMRoleResourceDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="922fc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="922fc-129">CommonParameters</span></span>
<span data-ttu-id="922fc-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="922fc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="922fc-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="922fc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="922fc-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="922fc-132">INPUTS</span></span>

## <span data-ttu-id="922fc-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="922fc-133">OUTPUTS</span></span>

## <span data-ttu-id="922fc-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="922fc-134">NOTES</span></span>

## <span data-ttu-id="922fc-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="922fc-135">RELATED LINKS</span></span>

[<span data-ttu-id="922fc-136">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="922fc-136">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="922fc-137">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="922fc-137">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="922fc-138">Satz-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="922fc-138">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


