---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006218"
---
# <span data-ttu-id="d705f-101">Stop-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="d705f-101">Stop-AzureStorSimpleJob</span></span>

## <span data-ttu-id="d705f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d705f-102">SYNOPSIS</span></span>
<span data-ttu-id="d705f-103">Beendet einen StorSimple-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="d705f-103">Stops a StorSimple job.</span></span>

## <span data-ttu-id="d705f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d705f-104">SYNTAX</span></span>

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d705f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d705f-105">DESCRIPTION</span></span>
<span data-ttu-id="d705f-106">Das Cmdlet **Stop-AzureStorSimpleJob** beendet einen laufenden StorSimple-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="d705f-106">The **Stop-AzureStorSimpleJob** cmdlet stops an on-going StorSimple job.</span></span>
<span data-ttu-id="d705f-107">Sie können Aufträge angeben, indem Sie eine Instanz-ID oder einen Auftragsnamen angeben.</span><span class="sxs-lookup"><span data-stu-id="d705f-107">You can specify a jobs by supplying an instance ID or a job name.</span></span>

## <span data-ttu-id="d705f-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d705f-108">EXAMPLES</span></span>

### <span data-ttu-id="d705f-109">Beispiel 1: Beenden von Aufträgen für ein Gerät</span><span class="sxs-lookup"><span data-stu-id="d705f-109">Example 1: Stop jobs for a device</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

<span data-ttu-id="d705f-110">Dieser Befehl ruft die Aufträge für das Gerät mit dem Namen Device07 mit dem Cmdlet **Get-AzureStorSimpleJob** ab.</span><span class="sxs-lookup"><span data-stu-id="d705f-110">This command gets the jobs for the device named Device07, by using the **Get-AzureStorSimpleJob** cmdlet.</span></span>
<span data-ttu-id="d705f-111">Der Befehl übergibt die Aufträge mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d705f-111">The command passes the jobs to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d705f-112">Das aktuelle Cmdlet beendet alle Aufträge, die der Befehl an ihn übergibt.</span><span class="sxs-lookup"><span data-stu-id="d705f-112">The current cmdlet stops any jobs that the command passes to it.</span></span>
<span data-ttu-id="d705f-113">Der Befehl gibt den Parameter *Force* an und fordert Sie daher nicht zur Bestätigung auf, bevor ein Auftrag beendet wird.</span><span class="sxs-lookup"><span data-stu-id="d705f-113">The command specifies the *Force* parameter, and, so, it does not prompt you for confirmation before it stops a job.</span></span>

### <span data-ttu-id="d705f-114">Beispiel 2: Beenden eines bestimmten Auftrags</span><span class="sxs-lookup"><span data-stu-id="d705f-114">Example 2: Stop a specific job</span></span>
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

<span data-ttu-id="d705f-115">Dieser Befehl beendet den Auftrag mit der angegebenen Instanz-ID.</span><span class="sxs-lookup"><span data-stu-id="d705f-115">This command stops the job that has the specified instance ID.</span></span>

## <span data-ttu-id="d705f-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="d705f-116">PARAMETERS</span></span>

### <span data-ttu-id="d705f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d705f-117">-Force</span></span>
<span data-ttu-id="d705f-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d705f-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d705f-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="d705f-119">-InstanceId</span></span>
<span data-ttu-id="d705f-120">Gibt die ID des Geräte Auftrags an, der beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d705f-120">Specifies the ID of the device job to stop.</span></span>

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

### <span data-ttu-id="d705f-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="d705f-121">-Profile</span></span>
<span data-ttu-id="d705f-122">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="d705f-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="d705f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d705f-123">CommonParameters</span></span>
<span data-ttu-id="d705f-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d705f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d705f-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d705f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d705f-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d705f-126">INPUTS</span></span>

### <span data-ttu-id="d705f-127">Keine</span><span class="sxs-lookup"><span data-stu-id="d705f-127">None</span></span>

## <span data-ttu-id="d705f-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d705f-128">OUTPUTS</span></span>

### <span data-ttu-id="d705f-129">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="d705f-129">DeviceJobDetails</span></span>
<span data-ttu-id="d705f-130">Dieses Cmdlet ruft Details des **DeviceJob** ab, das mit diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="d705f-130">This cmdlet gets details of the **DeviceJob** that this cmdlet stops.</span></span>

## <span data-ttu-id="d705f-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="d705f-131">NOTES</span></span>

## <span data-ttu-id="d705f-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d705f-132">RELATED LINKS</span></span>

[<span data-ttu-id="d705f-133">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="d705f-133">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


