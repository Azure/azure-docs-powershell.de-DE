---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 69FBF1E7-E69A-42B5-AC17-C7CF8CAB3C9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da323d5284de94aaadfc92abdf819f861695335
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007589"
---
# <span data-ttu-id="d6856-101">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="d6856-101">Set-WAPackVMRole</span></span>

## <span data-ttu-id="d6856-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d6856-102">SYNOPSIS</span></span>
<span data-ttu-id="d6856-103">Ändert die Eigenschaft instanzenanzahl einer Rolle des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="d6856-103">Changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="d6856-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6856-104">SYNTAX</span></span>

```
Set-WAPackVMRole -VMRole <VMRole> -InstanceCount <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6856-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6856-105">DESCRIPTION</span></span>
<span data-ttu-id="d6856-106">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="d6856-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="d6856-107">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d6856-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d6856-108">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d6856-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d6856-109">Das Cmdlet " **Satz-WAPackVMRole** " ändert die Eigenschaft "instanzenanzahl" einer Rolle für einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="d6856-109">The **Set-WAPackVMRole** cmdlet changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="d6856-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6856-110">EXAMPLES</span></span>

### <span data-ttu-id="d6856-111">Beispiel 1: Angeben der instanzenanzahl für eine Rolle eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="d6856-111">Example 1: Specify the instance count for a virtual machine role</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Set-WAPackVMRole -VMRole $VMRole -InstanceCount 3
```

<span data-ttu-id="d6856-112">Der erste Befehl ruft die Rolle des virtuellen Computers mit dem Namen ContosoVMRole01 mit dem Cmdlet **Get-WAPackVMRole** ab und speichert dieses Objekt dann in der $VMRole Variablen.</span><span class="sxs-lookup"><span data-stu-id="d6856-112">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="d6856-113">Mit dem zweiten und letzten Befehl wird die neue instanzenanzahl der Rolle des virtuellen Computers festgelegt, die in $VMRole auf 3 gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d6856-113">The second and final command sets the new instance count of the virtual machine role stored in $VMRole to 3.</span></span>

## <span data-ttu-id="d6856-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6856-114">PARAMETERS</span></span>

### <span data-ttu-id="d6856-115">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="d6856-115">-InstanceCount</span></span>
<span data-ttu-id="d6856-116">Gibt die Anzahl der Instanzen für eine Rolle eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="d6856-116">Specifies the instance count for a virtual machine role.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6856-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6856-117">-PassThru</span></span>
<span data-ttu-id="d6856-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d6856-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d6856-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="d6856-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6856-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="d6856-120">-Profile</span></span>
<span data-ttu-id="d6856-121">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d6856-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d6856-122">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d6856-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d6856-123">-VMRole</span><span class="sxs-lookup"><span data-stu-id="d6856-123">-VMRole</span></span>
<span data-ttu-id="d6856-124">Gibt eine Rolle für einen virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="d6856-124">Specifies a virtual machine role.</span></span>
<span data-ttu-id="d6856-125">Verwenden Sie zum Abrufen einer Rolle für einen virtuellen Computer das Cmdlet **Get-WAPackVMRole** .</span><span class="sxs-lookup"><span data-stu-id="d6856-125">To obtain a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6856-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6856-126">CommonParameters</span></span>
<span data-ttu-id="d6856-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6856-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6856-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6856-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6856-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d6856-129">INPUTS</span></span>

## <span data-ttu-id="d6856-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d6856-130">OUTPUTS</span></span>

## <span data-ttu-id="d6856-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="d6856-131">NOTES</span></span>

## <span data-ttu-id="d6856-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d6856-132">RELATED LINKS</span></span>

[<span data-ttu-id="d6856-133">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="d6856-133">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="d6856-134">Neu – WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="d6856-134">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="d6856-135">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="d6856-135">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)


