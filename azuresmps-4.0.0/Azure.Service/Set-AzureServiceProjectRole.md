---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5D093C10-F8B6-4F4A-ABD7-CC4D7AB7AFFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: c78f53b95d18de600535368a1109b318294928c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006158"
---
# <span data-ttu-id="adcf1-101">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="adcf1-101">Set-AzureServiceProjectRole</span></span>

## <span data-ttu-id="adcf1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="adcf1-102">SYNOPSIS</span></span>
<span data-ttu-id="adcf1-103">Legt die Anzahl der Instanzen oder die Laufzeitversion einer Rolle fest.</span><span class="sxs-lookup"><span data-stu-id="adcf1-103">Sets the number of instances or the runtime version of a role.</span></span>

## <span data-ttu-id="adcf1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="adcf1-104">SYNTAX</span></span>

### <span data-ttu-id="adcf1-105">Instanzen</span><span class="sxs-lookup"><span data-stu-id="adcf1-105">Instances</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Instances <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="adcf1-106">Runtime</span><span class="sxs-lookup"><span data-stu-id="adcf1-106">Runtime</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Runtime <String> -Version <String> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="adcf1-107">VMSize</span><span class="sxs-lookup"><span data-stu-id="adcf1-107">VMSize</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] [-PassThru] -VMSize <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="adcf1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="adcf1-108">DESCRIPTION</span></span>
<span data-ttu-id="adcf1-109">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="adcf1-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="adcf1-110">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="adcf1-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="adcf1-111">Das Cmdlet " **Set-AzureServiceProjectRole** " legt die Anzahl der Rolleninstanzen für die angegebene Rolle fest.</span><span class="sxs-lookup"><span data-stu-id="adcf1-111">The **Set-AzureServiceProjectRole** cmdlet sets the number of role instances for the specified role.</span></span>

## <span data-ttu-id="adcf1-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="adcf1-112">EXAMPLES</span></span>

### <span data-ttu-id="adcf1-113">Beispiel 1: Einrichten von Instanzen für eine webrolle</span><span class="sxs-lookup"><span data-stu-id="adcf1-113">Example 1: Set instances for a web role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWebRole" 2
```

<span data-ttu-id="adcf1-114">Legt die Anzahl der Instanzen für die Web-Rolle mit dem Namen MyWebRole1 auf 2 fest.</span><span class="sxs-lookup"><span data-stu-id="adcf1-114">Sets the number of instances for the web role named MyWebRole1 to 2.</span></span>

### <span data-ttu-id="adcf1-115">Beispiel 2: Einrichten von Instanzen für eine Worker-Rolle</span><span class="sxs-lookup"><span data-stu-id="adcf1-115">Example 2: Set instances for a worker role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWorkerRole1" 2
```

<span data-ttu-id="adcf1-116">Legt die Anzahl der Rolleninstanzen für die Worker-Rolle mit dem Namen WorkerRole1 auf 2 fest.</span><span class="sxs-lookup"><span data-stu-id="adcf1-116">Sets the role instance count for the worker role named WorkerRole1 to 2.</span></span>

### <span data-ttu-id="adcf1-117">Beispiel 3: Einrichten der Laufzeitversion für einen Rollendienst</span><span class="sxs-lookup"><span data-stu-id="adcf1-117">Example 3: Set the runtime version for a role service</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyRole1" node 0.6.20
```

<span data-ttu-id="adcf1-118">Legt die node.exe-Laufzeitversion für Role MyRole1 auf 0.6.20 fest.</span><span class="sxs-lookup"><span data-stu-id="adcf1-118">Sets the node.exe runtime version for role MyRole1 to 0.6.20.</span></span>

## <span data-ttu-id="adcf1-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="adcf1-119">PARAMETERS</span></span>

### <span data-ttu-id="adcf1-120">-Instanzen</span><span class="sxs-lookup"><span data-stu-id="adcf1-120">-Instances</span></span>
<span data-ttu-id="adcf1-121">Gibt die Anzahl der Rolleninstanzen für die angegebene Web-oder Worker-Rolle an.</span><span class="sxs-lookup"><span data-stu-id="adcf1-121">Specifies the number of role instances for the specified web or worker role.</span></span>

```yaml
Type: Int32
Parameter Sets: Instances
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adcf1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="adcf1-122">-PassThru</span></span>
<span data-ttu-id="adcf1-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="adcf1-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="adcf1-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="adcf1-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="adcf1-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="adcf1-125">-Profile</span></span>
<span data-ttu-id="adcf1-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="adcf1-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="adcf1-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="adcf1-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="adcf1-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="adcf1-128">-RoleName</span></span>
<span data-ttu-id="adcf1-129">Gibt den Namen der zu ändernden Web-oder Worker-Rolle an.</span><span class="sxs-lookup"><span data-stu-id="adcf1-129">Specifies the name of the web or worker role to be changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adcf1-130">-Runtime</span><span class="sxs-lookup"><span data-stu-id="adcf1-130">-Runtime</span></span>
<span data-ttu-id="adcf1-131">Gibt die Laufzeit an, die der angegebenen Rolle hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="adcf1-131">Specifies the runtime to add to the specified role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adcf1-132">-Version</span><span class="sxs-lookup"><span data-stu-id="adcf1-132">-Version</span></span>
<span data-ttu-id="adcf1-133">Gibt die Version der Common Language Runtime an, die der Rolle hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="adcf1-133">Specifies the version of the runtime to add to the role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adcf1-134">-VMSize</span><span class="sxs-lookup"><span data-stu-id="adcf1-134">-VMSize</span></span>
<span data-ttu-id="adcf1-135">Gibt die Größe des virtuellen Computers der Rolle an.</span><span class="sxs-lookup"><span data-stu-id="adcf1-135">Specifies the virtual machine size of the role.</span></span>

```yaml
Type: String
Parameter Sets: VMSize
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adcf1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adcf1-136">CommonParameters</span></span>
<span data-ttu-id="adcf1-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adcf1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adcf1-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adcf1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adcf1-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="adcf1-139">INPUTS</span></span>

###  
<span data-ttu-id="adcf1-140">Gibt die Größe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="adcf1-140">Specifies the size of the virtual machine.</span></span>

## <span data-ttu-id="adcf1-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="adcf1-141">OUTPUTS</span></span>

## <span data-ttu-id="adcf1-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="adcf1-142">NOTES</span></span>

## <span data-ttu-id="adcf1-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="adcf1-143">RELATED LINKS</span></span>

[<span data-ttu-id="adcf1-144">Satz-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="adcf1-144">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


