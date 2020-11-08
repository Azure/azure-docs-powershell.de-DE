---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8170AEF9-46E6-4087-8A68-29DFD5D014B5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb63d143ca2cafce92109e17fd3ced6a9dc070e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006030"
---
# <span data-ttu-id="c7301-101">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="c7301-101">Set-AzureRole</span></span>

## <span data-ttu-id="c7301-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7301-102">SYNOPSIS</span></span>
<span data-ttu-id="c7301-103">Legt die Anzahl der Instanzen einer Azure-Rolle fest, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7301-103">Sets the number of instances of an Azure role to run.</span></span>

## <span data-ttu-id="c7301-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7301-104">SYNTAX</span></span>

```
Set-AzureRole [-ServiceName] <String> [-Slot] <String> [-RoleName] <String> [-Count] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7301-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7301-105">DESCRIPTION</span></span>
<span data-ttu-id="c7301-106">Das Cmdlet " **Set-AzureRole** " legt fest, wie viele Instanzen einer angegebenen Rolle in einer Azure-Bereitstellung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c7301-106">The **Set-AzureRole** cmdlet sets the number of instances of a specified role to run in an Azure deployment.</span></span>

## <span data-ttu-id="c7301-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7301-107">EXAMPLES</span></span>

### <span data-ttu-id="c7301-108">1: die Anzahl der Instanzen für eine Rolle einstellen</span><span class="sxs-lookup"><span data-stu-id="c7301-108">1: Set the number of instances for a role</span></span>
```
PS C:\> Set-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestRole03" -Count 3
```

<span data-ttu-id="c7301-109">Mit diesem Befehl wird die MyTestRole03-Rolle festgelegt, die in Production für den MySvc01-Dienst ausgeführt wird, sodass drei Instanzen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c7301-109">This command sets the MyTestRole03 role that is running in production on the MySvc01 service to have three instances.</span></span>

## <span data-ttu-id="c7301-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7301-110">PARAMETERS</span></span>

### <span data-ttu-id="c7301-111">-Anzahl</span><span class="sxs-lookup"><span data-stu-id="c7301-111">-Count</span></span>
<span data-ttu-id="c7301-112">Gibt die Anzahl der Rolleninstanzen an, die ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c7301-112">Specifies the number of role instances to run.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7301-113">-Information</span><span class="sxs-lookup"><span data-stu-id="c7301-113">-InformationAction</span></span>
<span data-ttu-id="c7301-114">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="c7301-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c7301-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c7301-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7301-116">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="c7301-116">Continue</span></span>
- <span data-ttu-id="c7301-117">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="c7301-117">Ignore</span></span>
- <span data-ttu-id="c7301-118">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="c7301-118">Inquire</span></span>
- <span data-ttu-id="c7301-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c7301-119">SilentlyContinue</span></span>
- <span data-ttu-id="c7301-120">Beenden</span><span class="sxs-lookup"><span data-stu-id="c7301-120">Stop</span></span>
- <span data-ttu-id="c7301-121">Anhalten</span><span class="sxs-lookup"><span data-stu-id="c7301-121">Suspend</span></span>

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

### <span data-ttu-id="c7301-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c7301-122">-InformationVariable</span></span>
<span data-ttu-id="c7301-123">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="c7301-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c7301-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="c7301-124">-Profile</span></span>
<span data-ttu-id="c7301-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c7301-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c7301-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c7301-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c7301-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="c7301-127">-RoleName</span></span>
<span data-ttu-id="c7301-128">Gibt den Namen der Rolle an, für die die Anzahl der Instanzen festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7301-128">Specifies the name of the role for which to set the number of instances.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7301-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c7301-129">-ServiceName</span></span>
<span data-ttu-id="c7301-130">Gibt den Namen des Azure-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="c7301-130">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="c7301-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="c7301-131">-Slot</span></span>
<span data-ttu-id="c7301-132">Gibt die Bereitstellungsumgebung der Bereitstellung an, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7301-132">Specifies the deployment environment of the deployment to modify.</span></span>
<span data-ttu-id="c7301-133">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c7301-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7301-134">Produktions</span><span class="sxs-lookup"><span data-stu-id="c7301-134">Production</span></span>
- <span data-ttu-id="c7301-135">Inszenierung</span><span class="sxs-lookup"><span data-stu-id="c7301-135">Staging</span></span>

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

### <span data-ttu-id="c7301-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7301-136">CommonParameters</span></span>
<span data-ttu-id="c7301-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7301-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7301-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7301-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7301-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7301-139">INPUTS</span></span>

## <span data-ttu-id="c7301-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7301-140">OUTPUTS</span></span>

## <span data-ttu-id="c7301-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7301-141">NOTES</span></span>

## <span data-ttu-id="c7301-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7301-142">RELATED LINKS</span></span>

[<span data-ttu-id="c7301-143">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="c7301-143">Get-AzureRole</span></span>](./Get-AzureRole.md)


