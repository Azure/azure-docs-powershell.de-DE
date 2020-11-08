---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C50472E-CE36-4BF1-92C9-A3B9B183ACD1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 929b439c58c344a1902c497bbad6e056e3755025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006520"
---
# <span data-ttu-id="3c3d4-101">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="3c3d4-101">Get-AzureRole</span></span>

## <span data-ttu-id="3c3d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3c3d4-102">SYNOPSIS</span></span>
<span data-ttu-id="3c3d4-103">Gibt eine Liste der Rollen in Ihrem Microsoft Azure-Dienst zurück.</span><span class="sxs-lookup"><span data-stu-id="3c3d4-103">Returns a list of roles in your Microsoft Azure service.</span></span>

## <span data-ttu-id="3c3d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c3d4-104">SYNTAX</span></span>

```
Get-AzureRole [-ServiceName] <String> [[-Slot] <String>] [[-RoleName] <String>] [-InstanceDetails]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c3d4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c3d4-105">DESCRIPTION</span></span>
<span data-ttu-id="3c3d4-106">Das Cmdlet " **Get-AzureRole** " gibt ein Listenobjekt mit Details zu den Rollen in Ihrem Microsoft Azure-Dienst zurück.</span><span class="sxs-lookup"><span data-stu-id="3c3d4-106">The **Get-AzureRole** cmdlet returns a list object with details on the roles in your Microsoft Azure service.</span></span>
<span data-ttu-id="3c3d4-107">Wenn Sie den *roleName* -Parameter angeben, gibt **Get-AzureRole** nur Details zu dieser Rolle zurück.</span><span class="sxs-lookup"><span data-stu-id="3c3d4-107">If you specify the *RoleName* parameter, **Get-AzureRole** returns details on that role only.</span></span>
<span data-ttu-id="3c3d4-108">Wenn Sie den *InstanceDetails* -Parameter angeben, werden zusätzliche, instanzenspezifische Details zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3c3d4-108">If you specify the *InstanceDetails* parameter, additional, instance-specific details are returned.</span></span>

## <span data-ttu-id="3c3d4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c3d4-109">EXAMPLES</span></span>

### <span data-ttu-id="3c3d4-110">Beispiel 1: Abrufen einer Liste der Rollen für einen Dienst</span><span class="sxs-lookup"><span data-stu-id="3c3d4-110">Example 1: Get a list of roles for a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production"
```

<span data-ttu-id="3c3d4-111">Dieser Befehl gibt ein Objekt mit Details zu allen Produktions Rollen zurück, die im MySvc01-Dienst ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3c3d4-111">This command returns an object with details on all the production roles running on the MySvc01 service.</span></span>

### <span data-ttu-id="3c3d4-112">Beispiel 2: Abrufen von Details zu einer Rolle, die in einem Dienst ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="3c3d4-112">Example 2: Get details on a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc1" -Slot "Staging" -RoleName "MyTestVM3"
```

<span data-ttu-id="3c3d4-113">Dieser Befehl gibt ein Objekt mit Details zur MyTestVM3-Rolle zurück, die in der Staging-Umgebung des MySvc01-Diensts ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3c3d4-113">This command returns an object with details on the MyTestVM3 role, running on the staging environment of the MySvc01 service.</span></span>

### <span data-ttu-id="3c3d4-114">Beispiel 3: Abrufen von Instanzen Informationen zu Instanzen einer Rolle, die in einem Dienst ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="3c3d4-114">Example 3: Get instance information on instances of a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestVM02" -InstanceDetails
```

<span data-ttu-id="3c3d4-115">Dieser Befehl gibt ein Objekt mit Details zu den Instanzen der MyTestVM02-Rolle zurück, die in der Produktionsumgebung des MySvc01-Diensts ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3c3d4-115">This command returns an object with details on the instances of the MyTestVM02 role running in the production environment on the MySvc01 service.</span></span>

### <span data-ttu-id="3c3d4-116">Beispiel 4: Abrufen einer Tabelle mit den Rolleninstanzen, die einem Dienst zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="3c3d4-116">Example 4: Get a table of the role instances associated with a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -InstanceDetails | Format-Table -Auto "InstanceName", "InstanceSize", "InstanceStatus"
```

<span data-ttu-id="3c3d4-117">Dieser Befehl gibt eine Tabelle des Instanznamens, der Größe und des Status aller Rolleninstanzen zurück, die in der Produktionsumgebung des MySvc01-Diensts ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3c3d4-117">This command returns a table of the instance name, size, and status of all role instances running in the production environment on the MySvc01 service.</span></span>

## <span data-ttu-id="3c3d4-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c3d4-118">PARAMETERS</span></span>

### <span data-ttu-id="3c3d4-119">-Information</span><span class="sxs-lookup"><span data-stu-id="3c3d4-119">-InformationAction</span></span>
<span data-ttu-id="3c3d4-120">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="3c3d4-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3c3d4-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3c3d4-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3c3d4-122">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="3c3d4-122">Continue</span></span>
- <span data-ttu-id="3c3d4-123">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="3c3d4-123">Ignore</span></span>
- <span data-ttu-id="3c3d4-124">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="3c3d4-124">Inquire</span></span>
- <span data-ttu-id="3c3d4-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3c3d4-125">SilentlyContinue</span></span>
- <span data-ttu-id="3c3d4-126">Beenden</span><span class="sxs-lookup"><span data-stu-id="3c3d4-126">Stop</span></span>
- <span data-ttu-id="3c3d4-127">Anhalten</span><span class="sxs-lookup"><span data-stu-id="3c3d4-127">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c3d4-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3c3d4-128">-InformationVariable</span></span>
<span data-ttu-id="3c3d4-129">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="3c3d4-129">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c3d4-130">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="3c3d4-130">-InstanceDetails</span></span>
<span data-ttu-id="3c3d4-131">Gibt an, dass dieses Cmdlet Details zu den Instanzen für jede Rolle zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3c3d4-131">Specifies that this cmdlet returns details about the instances on each role.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c3d4-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="3c3d4-132">-Profile</span></span>
<span data-ttu-id="3c3d4-133">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3c3d4-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3c3d4-134">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3c3d4-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3c3d4-135">-RoleName</span><span class="sxs-lookup"><span data-stu-id="3c3d4-135">-RoleName</span></span>
<span data-ttu-id="3c3d4-136">Gibt den Namen der abzurufenden Rolle an.</span><span class="sxs-lookup"><span data-stu-id="3c3d4-136">Specifies the name of the role to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c3d4-137">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3c3d4-137">-ServiceName</span></span>
<span data-ttu-id="3c3d4-138">Gibt den Namen des Azure-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="3c3d4-138">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="3c3d4-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="3c3d4-139">-Slot</span></span>
<span data-ttu-id="3c3d4-140">Gibt die Azure-Bereitstellungsumgebung an.</span><span class="sxs-lookup"><span data-stu-id="3c3d4-140">Specifies the Azure deployment environment.</span></span>
<span data-ttu-id="3c3d4-141">Die akzeptablen Werte für diesen Parameter sind: Production oder Staging.</span><span class="sxs-lookup"><span data-stu-id="3c3d4-141">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c3d4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c3d4-142">CommonParameters</span></span>
<span data-ttu-id="3c3d4-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c3d4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c3d4-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c3d4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c3d4-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3c3d4-145">INPUTS</span></span>

## <span data-ttu-id="3c3d4-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3c3d4-146">OUTPUTS</span></span>

## <span data-ttu-id="3c3d4-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="3c3d4-147">NOTES</span></span>

## <span data-ttu-id="3c3d4-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3c3d4-148">RELATED LINKS</span></span>

[<span data-ttu-id="3c3d4-149">Satz-AzureRole</span><span class="sxs-lookup"><span data-stu-id="3c3d4-149">Set-AzureRole</span></span>](./Set-AzureRole.md)


